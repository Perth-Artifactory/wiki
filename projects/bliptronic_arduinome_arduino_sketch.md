---
title: Bliptronic Arduinome sketch
description: 
published: true
date: 2022-10-25T10:09:10.259Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:48:18.069Z
---

## What is this?

This is an [Arduino](http://www.arduino.cc/) sketch (program) for the [Bliptronic Arduinome](/projects/bliptronic_arduinome) project!

``` c
----
// Sam Hurst 2010.

// License: CC Attribution-Noncommercial-Share Alike 3.0 Uported http://creativecommons.org/licenses/by-nc-sa/3.0/



// PIN and PORT assignments

// If you're using hardware other than the unsped shield, you'll want to go through this portion of the code, 

// and change the pin numbers and atmega 168 PORTs that you're using.  We're using pin/PORT assignments here, 

// NOT the pin number scheme from the arduino board outputs (e.g. arduino digital pin 8 = PORTB pin 1)

// However, in the comments below, I do give the equivalents between arduino digital pin numbers and the 

// atmega168's PORT/bit numbering.



// #define ENABLE_DEBUG // uncomment for DEBUG



byte PORTB_Data_Direction = B11111100; // Inputs on 8, 9.

byte PORTC_Data_Direction = B00000000; // Analog Inputs

byte PORTD_Data_Direction = B00000010; // Inputs on 2 .. 7. SERIAL OUTPUT/INPUT on right-most bits.





// Disable pull-up resistors on button INPUT ports.

byte PORTD_PullUp = B00000011; // Buttons on Arduino pins 2 .. 7

byte PORTB_PullUp = B11111100; // Buttons on Arduino pins 8 .. 9.





// Common clock for ST_CP and LED_CLK (U3 & U5)

byte clockSTPin = 10;

byte clockSTMaskHigh = 1 << (clockSTPin & B00000111);

byte clockSTMaskLow = ~clockSTMaskHigh;

#define ST_CLOCK_PORT (PORTB)



// Common connection - data port for U3, U5, U7.

byte dataPin = 11;

byte dataMaskHigh = 1 << (dataPin & B00000111);

byte dataMaskLow = ~dataMaskHigh;

#define DATA_PORT (PORTB)



// Shift clock for U3 (Led data)

byte clockSHPin = 12;

byte clockSHMaskHigh = 1 << (clockSHPin & B00000111);

byte clockSHMaskLow = ~clockSHMaskHigh;

#define SH_CLOCK_PORT (PORTB)



// Clock for U7 (Buttons)

byte clockBTNPin = 13;

byte clockBTNMaskHigh = 1 << (clockBTNPin & B00000111);

byte clockBTNMaskLow = ~clockBTNMaskHigh;

#define BTN_CLOCK_PORT (PORTB)



// END pin and PORT assignments



// BUTTON PIN READ AND PORT ASSIGNMENT



// A read of 1 is a button being pushed.

// Readout from keypad is mapped:

// D17-D24 output to Arduino pin 08 (PORTD)

// D25-D32 output to Arduino pin 09 (PORTD)

// D33-D40 output to Arduino pin 02 (PORTD)

// D41-D48 output to Arduino pin 03 (PORTD)

// D49-D56 output to Arduino pin 04 (PORTD)

// D57-D64 output to Arduino pin 05 (PORTD)

// D65-D72 output to Arduino pin 06 (PORTB)

// D73-D80 output to Arduino pin 07 (PORTB)



#define BUTTON_MASK (((PIND) & B11111100) | ((PINB) & B00000011))  // In resultant byte, 1 = Button pushed. (Bit-order-to-Arduino-pin: 7, 6, 5, 4, 3, 2, 9, 8)



// ----------------------------



// Global variables 



byte byte0, byte1;                      // storage for incoming serial data

byte WaitingForAddress = 1;             // 1 when we expect the next serial byte to be an address value, 0 otherwise

byte address =  0x00;                   // garbage byte to hold address of function

byte state   =  0x00;                   // garbage byte to hold state value

byte x = 0x00;                          // garbage byte to hold x position

byte y = 0x00;                          // garbage byte to hold y position

byte z = 0x00;                          // garbage byte to iterate over buttons



#ifdef ENABLE_DEBUG

byte debug_array[3];

byte debug_ptr = 0;

#endif



byte display_test = B00000000;                 // non-zero value means display_test.



byte ShutdownModeChange = 0;            

byte ShutdownModeVal= 0;



// These variables are used to handle the ADC messages, and store which ports are currently enabled,

// and which are not.

byte adcEnableState[4];

int adcCurrent[4]; 

int adcTolerance = 4;



byte ledmem[8];                         // memory for LED states - 64 bits.



int b = 0;                              // temporary variable used in transmission of button presses/releases

int i = 0;                              // temporary variable for looping etc.

int id = 0;                             // temporary storage for incoming message ID



#ifdef ENABLE_DEBUG

byte debug_mode = 0;

#endif





#define BUTTON_ON_CONST (192)

#define BUTTON_OFF_CONST (64)

#define BUTTON_DEBOUNCE_CONST (32)



byte button_debounce[8][8];                // State of buttons each represented as value 0 .. 255 



byte button_row;

byte led_column;

byte buttons_pushed;



void ledLoad(byte led_data) { 

  byte mask;

  mask = 1;                                     // shifting counter

  do {

    if ((led_data & mask) | display_test) {       // check the status of bit, or is display_test on?

      DATA_PORT &= dataMaskLow;                 // Low means voltage drop across LED.

    }

    else {

      DATA_PORT |= dataMaskHigh;                // High means no voltage drop across LED.

    }

    waste();

    // Pulse the 595 Shift clock.

    SH_CLOCK_PORT |= clockSHMaskHigh;//    digitalWrite(clock, HIGH);   // "tock" input bit

    waste();

    SH_CLOCK_PORT &= clockSHMaskLow; //    digitalWrite( clock, LOW);   // "tick" prepeare for bit input

    waste();

    mask = mask << 1;

  } while (mask);                               // until shifting counter shifts left to a zero.

}



// memInit - helper function that zeros the button states and initialises the button clock.

void memInit() {

  byte k, l;

  for (k = 0; k < 8; k++) {

    ledmem[k] = 0;

    for ( l = 0; l < 8; l++) {

     button_debounce[k][l] = (BUTTON_OFF_CONST); 

    }

    DATA_PORT &= dataMaskLow;             // Bring data pin low.    

    ST_CLOCK_PORT |= (clockSTMaskHigh); // Clock through the low.

    ST_CLOCK_PORT &= (clockSTMaskLow);  // Clock through the low.

    DATA_PORT &= dataMaskLow;             // Bring data pin low.

    ST_CLOCK_PORT |= (clockBTNMaskHigh);  // Clock through the low.

    ST_CLOCK_PORT &= (clockBTNMaskLow); // Clock through the low.

  }

  button_row = 0;                       // First button row is powered.  

  led_column = 0;

}



// buttonRowCheck - checks and communicates changes in the current selected row of buttons. (8 buttons in a row = 1 byte)

void buttonRowCheck() { 

  byte button_read;

  byte j, mask, val;



  button_read = BUTTON_MASK;

  // Each button is a bit, use this input to debounce.

  j = 0;

  mask = 1;

  do {

    val = button_debounce[button_row][j];

    if (button_read & mask) {

      if (++val == BUTTON_ON_CONST) {

        Serial.print(B00000001, BYTE);                    // Message  Type: 0x0 (button change of state)    State: 0x1 (state=1).

        Serial.print((button_row << 4) | (j & 15), BYTE);  // Message  Address of button: xxxxyyyy

      }

    }

    else {    

      if (--val ==  BUTTON_OFF_CONST) {

        Serial.print(B00000000, BYTE);            // Message  Type: 0x0 (button change of state)    State: 0x0 (state=0).

        Serial.print((button_row << 4) | (j & 15), BYTE); // Message  Address of button: xxxxyyyy

      }

    }

    button_debounce[button_row][j] 

      =constrain(  val,

       BUTTON_OFF_CONST - BUTTON_DEBOUNCE_CONST,

       BUTTON_ON_CONST + BUTTON_DEBOUNCE_CONST);

    j++;

    mask = mask << 1;

  } while (mask);

}



// buttonClock - Generate 12.5% duty pulse on outputs of U7 (Button reading).

void buttonClock() {

  button_row = (button_row + 1) & 7;      // increment and modulo button_row.

  if (button_row) {                       // if we're back at the first row again (button_row = 0)

    DATA_PORT &= dataMaskLow;             // Bring data pin low - we need to make another low pulse.

  }

  else {                                  // if we're at the second through eighth rows (button_row = 1..7)

    DATA_PORT |= dataMaskHigh;            // Bring data pin high - it's a single clock pulse.

  }

  waste();

  BTN_CLOCK_PORT |= clockBTNMaskHigh;     // Clock the data pin through, advance to row.

  waste();

  BTN_CLOCK_PORT &= clockBTNMaskLow;      //

  waste();

}







// pulseClock - Generate 12.5% duty pulse to U5 (LED Column output).

//              Stores Shift Registers to Storage Registers (LED Status) for U3.

void pulseClock() {

  led_column = (led_column + 1) & 7;      // increment and modulo led_column.

  if (led_column) {                       // 

    DATA_PORT &= dataMaskLow;             // Bring data pin low if we're on rows 1 .. 7

  }

  else {                                  // 

    DATA_PORT |= dataMaskHigh;            // Bring data pin high if we're back at the beginning.

  }

  waste();

  ST_CLOCK_PORT |= clockSTMaskHigh;      // Clock the data pin through, advance to row.

  waste();

  ST_CLOCK_PORT &= clockSTMaskLow;       // 

  waste();

}



#define ISR_FREQ 5000     //~100Hz        // Sets the speed of the ISR - LOWER IS FASTER

//#define ISR_FREQ 1250     //~100Hz        // Sets the speed of the ISR - LOWER IS FASTER

                                          // Lowest safe rate:

                                          // Baudrate     = 57600bps = 7200 bytes per second

                                          // Buffer Size  = 128 bytes

                                          // Full buffers per second = 7200 / 128 = 56.25 Hz.

void setISRtimer(){  // setup ISR timer

  TCCR2A = (1<<WGM21);                    // WGM22=0 + WGM21=1 + WGM20=0 = Mode2 (CTC)

  TCCR2B = (1<<CS22)|(0<<CS21)|(1<<CS20); // set prescaler to /128(125kHz)

  TCNT2 = 0;                              // clear counter

  OCR2A = ISR_FREQ;                       // set TOP (divisor) - see #define

}



void startISR(){  // Starts the ISR

  TIMSK2=(1<<OCIE2A);                     // enable timer2 interrupt (calls ISR(TIMER2_COMPA_vect)

}



void stopISR(){    // Stops the ISR

  TIMSK2=(0<<OCIE2A);                     // disable timer2 interrupt

} 



ISR(TIMER2_COMPA_vect) {

  // first up: enable interrupts to keep the serial

  // class responsive

//  sei(); 

  while (Serial.available()) 

  {

    if (Serial.available())

    {

#ifdef ENABLE_DEBUG

      if (debug_mode) {

// START DEBUG CODE

        debug_array[debug_ptr] = Serial.read();

        debug_ptr++;

        if (debug_ptr == 3) { // have debug message, acceptable form: Dxyz, x = instruction, y = row, z = column.

          debug_ptr = 0;

          debug_mode = 0;

          WaitingForAddress = 1;

          switch (debug_array[0])

            {

              case 0 + 48:

                Serial.println(ledmem[debug_array[2] - 48],BIN);

                ledmem[debug_array[2] - 48] &= ~( 1 << (debug_array[1] - 48)); 

                Serial.println(ledmem[debug_array[2] - 48],BIN);

                Serial.println();

              break;

              case 1 + 48:

                Serial.println(ledmem[debug_array[2] - 48],BIN);

                ledmem[debug_array[2] - 48] |=  ( 1 << (debug_array[1] - 48));              

                Serial.println(ledmem[debug_array[2] - 48],BIN);

                Serial.println();

              break;

              case 2 + 48:

                Serial.println(ledmem[0],BIN);

                Serial.println(ledmem[1],BIN);

                Serial.println(ledmem[2],BIN);

                Serial.println(ledmem[3],BIN);

                Serial.println(ledmem[4],BIN);

                Serial.println(ledmem[5],BIN);

                Serial.println(ledmem[6],BIN);

                Serial.println(ledmem[7],BIN);

                Serial.println();

              break;

              case 3 + 48:

                for(i = 0; i < 8; i++) {

                  for(b = 0; b < 8; b++) {

                    Serial.print((byte)button_debounce[i][b],DEC);

                    Serial.print((byte)32,BYTE);

                  }

                  Serial.println();

                }

                  Serial.println();

              break;

              case 4 + 48:



                Serial.println((byte)PORTB,BIN);

                Serial.println((byte)PORTC,BIN);

                Serial.println((byte)PORTD,BIN);

                Serial.println((byte)PINB,BIN);

                Serial.println((byte)PINC,BIN);

                Serial.println((byte)PIND,BIN);

                Serial.println();

              break;

              case 5 + 48:

                Serial.println((byte)Serial.available(),DEC);

                Serial.println();

              break;

              case 6 + 48:

                Serial.println((byte)BUTTON_MASK,BIN);

                Serial.println();

              break;

              case 7 + 48:

                ledmem[debug_array[2] - 48] = 0; 

              break;

              case 8 + 48:

                ledmem[debug_array[2] - 48] = 255;                 

              break;

            }

        }

      }

      else {

#endif

// END DEBUG CODE

        if (WaitingForAddress == 1) {

          byte0 = Serial.read();

#ifdef ENABLE_DEBUG

          debug_mode = (byte0 == 68); // Arduino Serial I/O Monitor Debug mode. (48 = character 'D')

#endif

          address = byte0 >> 4;

          WaitingForAddress = 0;

        } // end if (WaitingForAddress == 1);

        else

        {

          WaitingForAddress = 1;

          byte1 = Serial.read();

  

          switch(address)

          {

          case 2: // set LED position x,y to state.

            state = byte0 & 15;

            x = 1 << (byte1 >> 4);

            y = byte1 & 15;

  

            if (state == 0){

              ledmem[y] &= ~(x); 

            }

            else {

              ledmem[y] |=  (x);

            }

            break;

//          case 3:

//            IntensityChange = 1;

//            IntensityVal = byte1 & 15;          

//            break;

          case 4:

            display_test = byte1 & 15;

            break;

          case 5:

            adcEnableState[(byte1 >> 4)&0x03] = byte1 & 15;

            break;

          case 6: 

            ShutdownModeChange = 1;

            ShutdownModeVal= byte1 & 15;

            break;

          case 7: // set LED row x to byte value y

            x = byte0 & 7;         // row. mask this value so we don't write to an invalid address.

            y = byte1;             // data

            ledmem[x] = y;

            break;

          case 8: // set LED column ??

            byte0 = 1 << (byte0 & 7);  // column. mask this value so we don't write to an invalid address.

            z = 0;

            x = 1;                     // shifting counter.

            do {

              if (byte1 & x) {

                ledmem[z] |= byte0; // 

              }

              else {

                 ledmem[z] &= ~byte0;

              }

              x = x << 1;              

            } while (x);               // until shifting counter shifts left to a zero.

            break;

           } // end switch(address)

        } // end else (WaitingForAddress = 0)

#ifdef ENABLE_DEBUG

      } // end else (!debug_mode)

#endif

    } // end else

  } // end while

}



void delay2(unsigned long delay_time)

{

  // reactivate overflow interrupt for

  // timer 1 - it's needed by delay() / millis()

  TIMSK0 |= (1 << TOIE0); 

  unsigned long start = millis();

  while (millis() - start <= delay_time)

  TIMSK0 &= ~(1 << TOIE0);

//  Disable timer.

}









void setup () {



  DDRD = PORTD_Data_Direction;

  DDRB = PORTB_Data_Direction;

  DDRC = PORTC_Data_Direction;



  PORTB = PORTB & PORTB_PullUp; // Ensure the pull-up resistors are disabled for button inputs on PORTB.

  PORTD = PORTD & PORTD_PullUp; // Ensure the pull-up resistors are disabled for button inputs on PORTD.



  memInit(); 



  Serial.begin(57600);

  setISRtimer();

  startISR();



}  



void loop () {

    ledLoad(ledmem[(led_column + 1) & 7]); // Load the status of next line.

    pulseClock(); // Move to next LED line.

    buttonClock();

    buttonRowCheck();



}



void waste() {

    volatile int slow = 0; 

    while (slow < 4) 

    { 

      slow++; 

    }

}
```
