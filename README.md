# WPCResources
Links, notes and other resources about WPC internals

## History
* [Williams Pinball Controller (WIKIPEDIA)](https://en.wikipedia.org/wiki/Williams_Pinball_Controller)
* [Williams WPC (PINWIKI)](https://www.pinwiki.com/wiki/index.php/Williams_WPC)

## WPC Internals

#### notes from *mrglee* (Garret Lee)  
originally from pinhacks.com (currently offline)

* [Match Values PDF](pdfs/WPC_MatchValue.pdf) (14 pages)
* [Lamp Matrix PDF](pdfs/WPCLampMatrix.pdf) (46 pages)
* [Transistors PDF](pdfs/WPCTransistors.pdf) (80 pages)
* [Adjustments PDF](pdfs/WPCAdjustments.pdf) (48 pages)
* [Adjustment Lockouts PDF](pdfs/WPC_AdjustmentLockouts.pdf) (34 pages)
* [Sound calls PDF](pdfs/WPCSoundCalls.pdf)  (59 pages)

* [Indexed Callbacks Table](pdfs/mrglee-notes-callbacks-table.md)
* [Easter Eggs Table Notes](pdfs/mrglee-notes-easter-eggs.md)
* ~~[DMD scroller](http://96.0.233.214/showthread.php?tid=77)~~
* [Solenoid notes](http://96.0.233.214/showthread.php?tid=76)
* [Coin vs Free play mods](http://96.0.233.214/showthread.php?tid=16)
* [Flipper Codes table](pdfs/mrglee-notes-easter-eggs.md)
* [Master Font Table](http://96.0.233.214/showthread.php?tid=23)
* [Disable POST](http://96.0.233.214/showthread.php?tid=2)
* [Checksum Hacks](http://96.0.233.214/showthread.php?tid=10)

#### notes from *maddes* (Matthias Buecher)
* [WPC Debugging](https://www.maddes.net/pinball/wpc_debugging.htm)

#### WPC Serial Port
* [WPC Serial Communications](WPC-serial-index.md)

### WPC Bench Test unit
* [Williams WPC 95 bench test (youtube)](https://www.youtube.com/watch?v=aBJBBL42gS8)

#### WPC LEDS Information
* [WPC LEDS Explained](https://www.pinball.co.uk/pinball-problems-2/wpc-leds-explained/)

#### WPC DCS Sound
* [FPGA DCS Project - Dr. Edward Cheung](http://www.edcheung.com/album/album07/Pinball/wpc_sound.htm)
* [Notes on DCS format / WPC DSP chip](wpc-dcs-audio-format-notes.md)

### WPC Hardware Repair Guide
* [WPC Repair Guide](http://www.pinballsupernova.com/Williams%20Repair%20Guide/Williams%201990-1999%20WPC.pdf)

## Other Williams Pin Platforms
### System 11 Internals notes from *Francis*
* [System 11 debugging](http://pinhacks.com/showthread.php?tid=80)
* [System 11 scoring](http://pinhacks.com/showthread.php?tid=82)

### Williams Level 7 Internals notes from *jaskey*
* [Williams Level 7 Programming Guide](http://gamearchive.askey.org/Pinball/Manufacturers/Williams/PinBuilder/text/williams_lvl7_programming.html)
* [System 7 Macro Codes](http://gamearchive.askey.org/Pinball/Manufacturers/Williams/PinBuilder/text/sys7_macros.txt)
* [System 7 Macro Codes - Summary Card](http://gamearchive.askey.org/Pinball/Manufacturers/Williams/PinBuilder/text/sys7_macrocard.txt)
* [System 7 Fix Guide (PDF: 14 pages)](http://arcarc.xmission.com/Pinball/PDF%20Pinball%20Misc/System%207%20Fix%20Guide.pdf)
* [System 7 Games (IPDB)](http://www.ipdb.org/search.pl?mpu=4&qh=checked&ng=checked&sortby=date&searchtype=advanced)

## MAME / PinMAME
### MAME Serial Ports
* [Serial Ports in MAME](https://frakaday.blogspot.com/2016/05/serial-ports-in-mame-part-i.html)
* [Connect a Serial Port to a MAME Board Driver](https://frakaday.blogspot.se/p/serial-port-in-mame.html)

### MAME Debugger
* [Scripting MAME via LUA](http://docs.mamedev.org/techspecs/luaengine.html)
* [MAME LUA script for COIN 1 RAM search](http://www.mamecheat.co.uk/forums/viewtopic.php?t=12245)

### PinMAME Debugger 
* [Debugger HELP](PinMAME/pinmame-debugger-help.md)
* [PinMAME nvRAM Maps](https://github.com/tomlogic/pinmame-nvram-maps)

### PinMAME Machine Simulators
* Pinball Simulator Start Template (PSST) - [source](https://github.com/vpinball/pinmame/blob/master/src/wpc/sims/template/psst.c)

## 6809 Resources
* [Assist09 on GitHub](https://github.com/jefftranter/6809/tree/master/sbc/assist09)
* [Assist09 Monitor and Forth asm source code](http://home.hccnet.nl/a.w.m.van.der.horst/m6809.html)
* [6809 Emulation Page](http://atjs.mbnet.fi/mc6809/#Info)
* [6809 OpCodes (alphabetical order)](6809opsalpha.md)
* [6809 OpCodes (numeric order)](6809opsnumeric.md)
* [6809 Programming Model and Registers](https://www.sbprojects.net/sbasm/6809.php)

## Other Hardware / Software projects 
### WPC-EMU
* [WPC-EMU on GitHub](https://github.com/neophob/wpc-emu)
* 
### FreeWPC
* [WPC Hardware Description](http://bcd.github.io/freewpc/The-WPC-Hardware.html#The-WPC-Hardware)
* [FreeWPC Serial Port Debugging](http://bcd.github.io/freewpc/Debugging.html)

### FlipProjets
* [WPC PIC Security Chip](https://www.flipprojets.fr/SecurityChip_EN.php)
* [WPC Prototype board](https://pinside.com/pinball/forum/topic/wpc-95-cpu-prototype-board)

### Robotron:2084
* [Disassembly notes and Interview](http://www.robotron2084guidebook.com/technical/christiangingras/)

### Disassembly / Reverse Engineering
* [Binary Ninja - Low-Level IL Explanation](https://blog.trailofbits.com/2017/01/31/breaking-down-binary-ninjas-low-level-il/)
