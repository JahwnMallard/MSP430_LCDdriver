# LCD Driver

## API

- `void initSPI();`
	- Initialize the SPI subsystem of the MSP430
- `void LCDinit();`
	- Initialize the LCD screen of the MSP430
- `void LCDclear();`
	- Clear the LCD screen
- `void cursorToLineTwo();`
	- sets the cursor to the beginning of the bottom line
- `void cursorToLineOne();`
	- sets the cursor to the beginning of the top line
- `void writeChar(char asciiChar);`
	- writes a character at the current cursor position
- `void writeString(char * string, int length);`
	- writes a string at the current cursor position of a given length
- `void scrollString(char * string1, char * string2, int message1Length, int message2Length);`
	- scrolls string 1 across the top line, scrolls string 2 across the bottom




