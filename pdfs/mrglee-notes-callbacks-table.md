WPC Indexed Callbacks Table
---------------------------

##### by MRGLEE (Garrett Lee) 

from pinhacks.com (currently offline)

RE: Challange: DM

The WPC code has sort of a master table of indexed callback functions for different features. 
Code can call this function by passing in the desired function index as a parameter byte (byte after the jsr opcode) 
or code can call the function directly with the desired index in the A register.

The function that takes the parameter byte looks something like the following. 
All it does it grab that parameter byte, puts it into the A register, then calls 
the real feature lookup function (shown below is snippet from dm_lx4):

```
85FE: 34 22             PSHS Y,A
8600: 10 AE 63          LDY $0003,S
8603: A6 A0             LDA ,Y+
8605: 10 AF 63          STY $0003,S
8608: BD C7 B4          JSR $C7B4
860B: 35 A2             PULS A,Y,PC
```

Most of the callback routines ultimately check if a game is in progress, and if not, do nothing, 
so first start up a game so that you can observe how different functions behave. 

Then set a breakpoint at `$C7B4`. 

Then hit '5' to coin-up or just wait a few seconds since the game will keep calling this function every few seconds to say "PRESS LAUNCH" on the dmd. 

When the breakpoint is hit, look at the A-register which is the callback index. 

What we do next is simply modify value in A register then hit 'esc' to let the code continue and see what happens. 

This lets you determine the callback index for various features during game play. 

Once you know the callback index for the part of the game you want to modify, you need to do a litte deeper investigation which I'll describe later if I get some more free time.

Here is a summary of some function callback indexes that I derived from dm_lx4

```
0x02 game startup
0x0C show credits press start/insert coin message
0x0D tilt-warning
0x0F TILT
0x10 End-of-ball bonus
0x11 Shoot Again
0x16 Volume adjust
0x4a capture simon mode
0x4b jackpot increased
0x4d prison break
0x4e prison break triple
0x4f argentina?
0x50 3-million
0x52 explode hurry-up award
0x53 extra ball award
0x54 replay award
0x55 explode ramp added
0x56 computer: accessing/award
0x57 computer: next award
0x58 tripe car crash
0x59 retna scan 2x
0x5a bonus award
0x5b expode millions
0x5c super jets increased
0x5d laser millions
0x5e retna scan value grow
0x5f coin-door open message
0x60 game-over buy-in period
0x61 player 1 is up
0x62 buy-in cancelled by start button
0x63 buy-in cancelled by flippers
0x64 buy-in cancelled by launch button
0x65 car chase animation
0x66 Double car-crash award
0x67 super jackpot lit
0x69 U look gr8 2day
0x6a extra ball lit 
0x6c Double combo
0x6d Demolition Time status
0x6e Demolition Time startup
0x6f explosion/jackpot-award
0x70 Demolition Time Champion
0x71 Demolition Jackpot
0x72 PRESS LAUNCH message
0x73 Jackpot increased
0x74 Jump from helicopter animation,3Million
0x75 Quick Freeze enabled
0x76 Rats at 8 graffiti
0x77 Complete awards to light demolition time
0x78 Complete MTL to light claw
0x79 Complete yellow targets
0x7a Shoot value increased
0x7b Smithers eyeball bonus
0x7c Feel Great Bonus
0x7d Eat at Joes graffiti
0x7e Capture bonus
0x7f Simon Captured
0x80 Reply At
0x81 Jackpot added
0x82 Car chase
0x83 Wag graffiti
0x84 Demolition Jackpot is lit
0x85 Huxley award
```

Basically what we would do is find when the function gets called around the feature you want to modify and go from there...
