# 32K ROM/32K RAM Memory card
This is a RC2014 compatible memory card built on stripboard.
The card contains 32K ROM and 32K RAM. ROM occupies address 0x0000-0x7FFF. RAM occupies the upper half and is selected when A15 is high.
You can find Fritzing files above and diagrams and finished pictures below.

## Components
* Stripboard card (40 x 25 holes used here)
* 40 pin right angle header for RC2014 bus
* DIP socket x 2
* DIP 28 wide socket x 1
* DIP 28 narrow socket x 1
* 28256 type EEPROM (32Kx8)
* 71256 type SRAM (32Kx8)
* 74HC04 hex inverter IC
* 74HC32 quad OR IC

## Comments
1. 32K ROM is more than necessary, but was selected to simplify addressing. A15 low = ROM, A15 high = RAM. 
With some more card real estate, you could add some pull up resistors, jumpers, and diodes to the upper lines of the EEPROM to allow bank selection. 
This would allow you have multiple programs installed on a single EEPROM.
2. A more memory conscious approach would contain a small ROM that writes itself to another SRAM then enables the SRAM to allow full 64k of RAM.
Perhaps an output port could be used to control the CS and OE lines of the EEPROM and second SRAM.
3. Use HC or HCT series chips even though the diagram says LS.

## Photos
### Bottom side, trace cuts
![Bottom view, solder side](https://github.com/thavelka/Z80Boards/blob/master/memory/32kramrom_board.png)
### Component side, links only
![Top view, links](https://github.com/thavelka/Z80Boards/blob/master/memory/32kramrom_links.png)
### Component side, complete board
![Top view, complete](https://github.com/thavelka/Z80Boards/blob/master/memory/32kramrom_wires.png)
### Completed board
![Complete board](https://github.com/thavelka/Z80Boards/blob/master/memory/finished.jpg)
### Completed board, solder side
![Complete board](https://github.com/thavelka/Z80Boards/blob/master/memory/solderside.jpg)
