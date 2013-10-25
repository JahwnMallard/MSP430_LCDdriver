```c
/*
 * Author: C2C John Miller
 * Driver library for the MSP430 LCD screen
 */


/*---------------------------------------------------
 Function Name: INITSPI
 Author: C2C John Miller, USAF
 Function: Initializes the SPI of the MSP430
 Inputs: none
 Outputs: none
 Subroutines used: none
 ---------------------------------------------------*/
void initSPI();

/*---------------------------------------------------
 Function Name: LCDinit
 Author: Capt Todd Branchflower, USAF
 Function: Initializes the LCD screen of the MSP430
 Inputs: none
 Outputs: none
 Subroutines used: none
 ---------------------------------------------------*/
void LCDinit();

/*---------------------------------------------------
 Function Name: LCDclear
 Author: Capt Todd Branchflower, USAF
 Function: Clears the LCD screen of the MSP430
 Inputs: none
 Outputs: none
 Subroutines used: none
 ---------------------------------------------------*/
void LCDclear();

/*---------------------------------------------------
 Function Name: cursorToLineTwo
 Author: C2C John Miller, USAF
 Function: set the cursor to the beginning of the bottom half of the LCD
 Inputs: none
 Outputs: none
 Subroutines used: cursorToLineOne, writeCommandByte
 ---------------------------------------------------*/
void cursorToLineTwo();

/*---------------------------------------------------
 Function Name: cursorToLineTwo
 Author: C2C John Miller, USAF
 Function: set the cursor to the beginning of the top half of the LCD
 Inputs: none
 Outputs: none
 Subroutines used: writeCommandByte
 ---------------------------------------------------*/
void cursorToLineOne();

/*---------------------------------------------------
 Function Name: writeChar
 Author: C2C John Miller, USAF
 Function: Writes a single character
 Inputs: asciiChar
 Outputs: none
 Subroutines used: writeCommandByte, writeDataByte
 ---------------------------------------------------*/
void writeChar(char asciiChar);

/*---------------------------------------------------
 Function Name: writeString
 Author: C2C John Miller, USAF
 Function: Writes a string of characters
 Inputs: string, length
 Outputs: none
 Subroutines used: writeChar
 ---------------------------------------------------*/
void writeString(char * string, int length);

/*---------------------------------------------------
 Function Name: scrollString
 Author: C2C John Miller, USAF
 Function: Scrolls a message across the top of the lcd screen.
 Inputs: string1, string2, message1Length
 Outputs: none
 Subroutines used: writeString
 ---------------------------------------------------*/
void scrollString(char * string1, char * string2, int message1Length,
		int message2Length);

/*---------------------------------------------------
 Function Name: SET_SS_HI
 Author: C2C John Miller, USAF
 Function: ; Sets slave select to high (disabled) on the LCD
 Inputs: none
 Outputs: none
 Subroutines used: none
 ---------------------------------------------------*/
void set_SS_Hi();

/*---------------------------------------------------
 Function Name: SET_SS_LO
 Author: C2C John Miller, USAF
 Function: ; Sets slave select to low (enabled) on the LCD
 Inputs: none
 Outputs: none
 Subroutines used: none
 ---------------------------------------------------*/
void set_SS_Lo();

/*---------------------------------------------------
 Subroutine Name: SPI_send
 Author: Capt Todd Branchflower, USAF
 Function: Send a byte to the SPI for either commands or data
 Outputs: none
 Subroutines used: set_SS_hi, set_SS_lo
 ---------------------------------------------------*/
void SPI_send(char byteToSend);

/*---------------------------------------------------
 Subroutine Name: LCD_write_8
 Author: Capt Todd Branchflower, USAF
 Function: Send full byte to LCD
 Inputs: byteToSend
 Outputs: none
 Subroutines used: LCD_write_4
 ---------------------------------------------------*/
void LCD_write_8(char byteToSend);

/*---------------------------------------------------
 Subroutine Name: LCD_write_4
 Author: C2C John Miller, USAF
 Function: Send 4 bits of data to LCD via SPI.
 sets upper four bits to match LCDCON.
 Inputs: byteToSend
 Outputs: none
 Subroutines used: LCD_write_4
 ---------------------------------------------------*/
void LCD_write_4(unsigned char byteToSend);

/*---------------------------------------------------
 Function Name: delayMicro
 Author: C2C John Miller, USAF
 Function: Delays the MSP430 by 40.5 microseconds
 Inputs: none
 Outputs: none
 Subroutines used: __delay_cycles()
 ---------------------------------------------------*/
void delayMicro();

/*---------------------------------------------------
 Function Name: delayMilli
 Author: C2C John Miller, USAF
 Function: Delays the MSP430 by 1.65 milliseconds
 Inputs: none
 Outputs: none
 Subroutines used: __delay_cycles()
 ---------------------------------------------------*/
void delayMilli();
```
