# WPC Printer Kit 16-9464

The printer kit contains:

* A-14565-1 Printer Controller Board
* A-14619-1 Printer Interface Board
* 5795-12851-00  Data Communications Cable
* H-14682   Main Printer Cable
* 5795-12848-00  Parallel Printer Cable
* 16-9464   Manual (which contains instructions in English, German, and French)

The Data Communications Cable is a 34-pin daisy-chained ribbon cable; it plugs into:
* the CPU board at J202
* the Printer Controller Board at J701
* the Sound Board at J506
* and the Dot Matrix Controller Board at J602.

(If I recall correctly, these are already connected; the replacement cable has one more connector, for the printer board)

The Parallel Printer Cable is a 26-pin straight ribbon cable; it goes: 
* from J703 on the Printer Controller board 
* to J708 on the Printer Interface Board.

The Main Printer Cable provides the Serial Printer data, the German Printer data and the Power for the Printer Kit:

* The Serial Printer data uses 10-pin connectors, from J704 on the Printer Controller Board to J707 on the Printer Interface Board.
* The German Printer data uses 6-pin connectors, from J705 on the Printer Controller Board to J706 on the Printer Interface Board.
* J702 on the Printer Controller Board is power; 
    * it goes to J116 and J106 on the Power Driver Board 
    
    (which may already have connectors; there's a "Z-header" to allow the new cable to be connected, and the old connector attaches to the Z-header.

    (The instructions say J116, but the schematic says J118.  According to my TAF schematic, J116, J117, and J118 are the same; they all carry GND, +5 V, and +12 V so any of these could be used)

The Printer Controller board mounts above the CPU Board, to the left of the Sound Board.  
There may already a Fliptronic II Flipper board here; there are standoffs for mounting 
the printer board over the flipper board.

The Printer Interface board is just a set of connectors: 

* DB9 male for RS-232, 
* DB9 Female for "NSM", 
* DIN-8 for "ADP/Drucker" (from context, I'm guessing that "Drucker" is "printer") 
* and DB25 for parallel.  

The "NSM" and "ADP/Drucker" are presumably the "German" printers; 

### DIN-8 has: 

* +32V 
* +18V 
* GND 
* TxD 
* and RxD 

### "NSM Printer" has: 

* +18V 
* GND 
* TxD 
* RxD
* and DSR 

If you don't have this board or the cables, you can probably make up a cable that ends in the appropriate connector.