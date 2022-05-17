MAME vs PinMAME for Reversing
=============================

In the past PinMAME was the only choice because WPC ROMs were only supported there not in MAME.  This was true around the time Maddes wrote his debugging piece.  

Additionally special PinMAME and MAME builds used to be the only way to use the MAME debugger -- the MAME debugger was not included in all builds.


Advantages of MAME 
* MAME debugger is included in ALL builds
* LUA scripting support 
* Source code readily available
* Easier to build than PinMAME

Disadvantages of MAME  
* State of mechanical Game drivers is incomplete
    * Limited bindings for keyboard-to-physical-switch
    * No ball handling


* Updated how to retrieve PinMAME source code from Subversion repository.
* PinMAME 2.2 has been released. Executables with MAME Debugger are available too on Sourceforge.
* Hard-to-get current DEBUG releases
* Hard-to-build
    * Old Visual Studio examples
    * Old SDKs for Win and/or DirectX


MADDES ASSERTION (HOW-TO log WPC bankId in MAME using TRACE): 
> Unfortunately you can not log the content of a memory address with TRACE, so you don't know the bank of the code from $4000 to $7FFF, but you can search for the bytes of the code in the Game ROM to find out.    

MADDES ASSERTION (mystery bankId $18): 
> Other weird FPS constructs are calls of functions in non-existant banks, in IJ L-7 of bank $18 (try PinMAME: WP 0011 18). These FPS really work, as unused conductors, which depend on the ROM size, always have high voltage (=bit set). For IJ L-7 bank $18 leads to bank $38.
Below is "jmpPagedFunc" in hex values and 6809 assembler with comments.

    
MADDES:  
#### Debugging game functions
Most of the time you will be interested what happens when a special function is started in a game. The best way to do this is to exit the debugger, hit all switches necessary to start the function in the emulation, but get back into the debugger before or directly after you strike the last switch. Use the TRACE command to log what addresses are executed during this function. Unfortunately you can not log the content of a memory address with TRACE, so you don't know the bank of the code from $4000 to $7FFF, but you can search for the bytes of the code in the Game ROM to find out.

#### The three "call a bank function" routines
Another way to find functions inside a WPC ROM is to debug three routines (I named them "call a bank function" routines) which are in each and every WPC ROM. These routines are used when another function is called. As the target function could be within another bank, these routines care about switching the bank and calling the target function. The JSR routines also care about restoring the previous bank if necessary and jumping back to the original calling code. 

To find these routines search for the byte sequence "6E 9F 00 12" (=jmp [$0012]) in the System ROM, as this is always the last command of all three routines.

All three routines use a simple general purpose structure I named "Pointer Structure" (PS), this structure is used to point to functions (FPS) and data (DPS):

Format	Description
word	address of target
byte	bank of target
#$FF means a System ROM or dynamically selected target

The calls to the three routines are done very tricky with a FPS, or a pointer to one, directly behind the calling JSR, hence totally confusing disassemblers because of mixed code and data. 

My Java package WPC_Tool can create corresponding symbol files for DASMx, so the disassembler doesn't get confused, but there could also be some false positives (e.g. in graphics).

Other weird FPS constructs are calls of functions in non-existant banks, in IJ L-7 of bank $18 (try PinMAME: WP 0011 18). These FPS really work, as unused conductors, which depend on the ROM size, always have high voltage (=bit set). For IJ L-7 bank $18 leads to bank $38.
Below is "jmpPagedFunc" in hex values and 6809 assembler with comments.


### Macro Handling for Non-Standard call parameters

MADDES "call a bank function" routines

* `JSR_BANK`
* `JMP_BANK`
* `JSR_BANKADDRESS_AT`