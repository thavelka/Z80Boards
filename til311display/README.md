# TIL311 Hexadecimal Display
This is a RC2014 compatible display built on stripboard. More instructions and information [here](https://thavelka.io/2020/06/4-byte-til311-display-card/).
The card can display four bytes of data using eight TIL311 hexadecimal displays. 
This card works as an output device and occupies ports 0-3. 
You can find Fritzing files above with and without the data wires, for a better view of what's below the rat nest. 

## Components
* Stripboard card (40 x 24 holes used here)
* 40 pin right angle header for RC2014 bus
* Female machined breakaway headers, 7 pins x 16 pieces
* TIL311 display x 8
* 74138 IC for port address decoding
* 74541 IC for data bus buffering
* 1N914 or 1N4148 switching diodes x 6
* 10k-ish pull-down resistor x 1

## Comments
1. The TIL311s are difficult to use on stripboard due to the pins being oriented vertically. 
HP offered a similar display in a horizontal DIP8 package, although it is smaller. The TIL311 will just require tedious trace cutting.
2. The TIL311 has support for blanking and showing decimal points, but those features are not used here. 
Since the card occupies 8 address spaces and only four are used, you could add two octal latches to occupy to ports 4 and 5 for blanking and decimal support.

## Photos
### Bottom side, trace cuts
![Bottom view, solder side](https://github.com/thavelka/Z80Boards/blob/master/til311display/display_solder.png?)
### Component side, complete board
![Top view, complete](https://github.com/thavelka/Z80Boards/blob/master/til311display/displayschematic.png)
### Completed board
![Complete board](https://i2.wp.com/thavelka.io/wp-content/uploads/2020/06/IMG_20200624_230447.jpg)
