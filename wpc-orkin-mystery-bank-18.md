WPC Mystery Bank $18 (Orkin?)
=============================

* Is this bank/page `$18` where Orkin lives?
* Is referenced by more than ErrorHandling routine
* In a ROM that is large enough to have a native bank `$18`, i.e CV the contents are interesting
* Calls to $18 page
* Ram $031e and $031f relationship
* DEBUG ports relationship

`FFD0` vector with `00 00` 
`FFD2` vector with `00 00` 

`$18` -> `$38` when forced in NBAF

$561b, $3b

8051
8050

89cf loads X from Post-byte parameters
  then calls $5535, $3b

Test for $031f == 0 
	JSR 403F ; after setting bank to $18
	
JSR 904f  ; input examples: $20, $21, $22, $23, etc.
  A has return code, either 0 or 3
  
$18 == b 0001 1000
$20 == b 0010 0000
$38 == b 0011 1000

$3e == b 0011 1110
$3f == b 0011 1111
$ff == b 1111 1111



https://pinside.com/pinball/forum/topic/wpc-95-cpu-prototype-board


Hello all !

Have you ever seen a wpc-95 prototype board ?
This board comes with a security pic "generic apple" 123.
Never seen this code number for a game.
Unfortunably, this board comes with CONGO eprom, so off course, the board can boot with a know eprom, but no run as the message G10 fails appears.
CONGO is the first WPC-95 game, it seems logical to find the rom on this board.
The security pic works fine, we haven't yet found if there is some differences between the production pic.
Is there anybody who know about this 123 version ?
We are looking for 123 eprom ... If anybody has some information about its, you welcome !

The Flipprojets Team.




This prototype board has also some modifications:

The 150 ohms resistors R118, R119, R120 and R121 have been replaced by 0 ohm straps.
The RAM is not a 8 KB like on others WPC-95, but a 32 KB, like on earlier WPC-S with DCS sound.
The W3 and W7 straps are installed, providing full access to the RAM pages, using BANK1/BANK2 signals from ASIC.
There is a special pin for plugin. Located near the pin 32 of the G11 EPROM socket, and connected to the ROMW signal from ASIC. The W5 strap is installed while W4 not, thus the EPROM is powered by VBATT instead of VCC.
Replacement of the R118..R121 looks logical, as there is no reason to install resistors on the E and Q lines, between ASIC/CPU/74LS14.

RAM capacity is maximized, may be for testing, but not used on production games.




https://pinside.com/pinball/forum/topic/who-dunnit-prototype

https://pinside.com/pinball/forum/topic/wpc-95-cpu-prototype-board