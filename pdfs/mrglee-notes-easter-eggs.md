```
;----------------------------------;--------------------------------------------
;
;
; Easter egg checker.
;
; Called after earlier code has "latched in a
; number of right flipper presses.
;
615F: 34 76         PSHS U,Y,X,B,A  ;
6161: 32 7D         LEAS $FFFD,S    ; // Make room on stack for 3 local bytes
6163: 8E 61 99      LDX #$6199      ; X = 0x6199 // start of table, below
6166: BD AD 58      JSR $AD58       ; // Gets first 2 bytes from table into Y
6169: 10 AF E4      STY ,S          ; // this is the number of table entries.
616C: 6F 62         CLR $0002,S     ; // S+2 is our "i" variable for the loop below, init to zero
;
616E: 10 8E 05 E1   LDY #$05E1      ; Y = 0x05E1 // Address of right flipper press count
;
6172: A6 62         LDA $0002,S     ; for (i = 0; i < TableEntries; i++)
6174: A1 61         CMPA $0001,S    ; {
6176: 24 1D         BCC $6195       ; // A-register has the value of "i", current 0-based table index
6178: 8E 61 99      LDX #$6199      ; X = 0x6199 // start of table below
617B: BD AD 46      JSR $AD46       ; // Function to advance X to the "Ath" entry in the table below
617E: EE 89 00 02   LDU $0002,X     ; U = Table entry bytes 3&4. Address of Easter Egg function.
6182: AE 89 00 00   LDX $0000,X     ; X = Table entry bytes 1&2. Address of flipper button combination.
6186: 86 03         LDA #$03        ; A = 0x03 // Number of right flipper latches to check?
6188: BD A6 24      JSR $A624       ; // Function that sees if we have a hit on this table entry.
618B: 26 04         BNE $6191       ; if (EasterEggHit == True) // Z-bit means we have a hit
; {
618D: AD C4         JSR ,U              ; // Call the Easter Egg function!
618F: 20 04         BRA $6195           ; return;
6191: 6C 62         INC $0002,S         ; }
6193: 20 DD         BRA $6172           ; }
6195: 32 63         LEAS $0003,S        ;
6197: 35 F6         PULS A,B,X,Y,U,PC   ;
;
;--------------------------------;-------------------------------------------------
;
6199: 00 05             ; Table entries
619B: 04                ; bytes per entry
;
619C: 61 B0 61 BF       ; entry 0

61A0: 61 B3 62 78       ; entry 1

61A4: 61 B6 64 D9       ; entry 2

61A8: 61 B9 64 E1       ; entry 3

61AC: 61 BC 64 6D       ; entry 4

61B0: 05 01 05          ; entry 5
                        ; 5R + 1L + 1R + 1L + 5R + 1L, Call $61BF, Design Team

61B3: 0C 05 04          ; entry 6
                        ; 12R + 1L + 5R + 1L + 4R + 1L, Call $6278, Special thanks

61B6: 10 0D 0C          ; entry 7
                        ; 16R + 1L + 13R + 1L + 12R + 1L, Call $64D9, ?

61B9: 01 02 03          ; entry 8
                        ; 1R + 1L + 2R + 1L + 3R + 1L, Call $64E1, ?

61BC: 0F 08 03          ; entry 9
                        ; 15R + 1L + 8R + 1L + 3R + 1L, Call $646D, ?
;
;--------------------------------;-------------------------------------------------
```
So we have 3 unknown functions:
`$64D9`, `$64E1`, and `$646D`.

Below are partially annotated functions for `$64D9` and `$64E1`:

```
;----------------------------------------;-----------------------------------------
;
64D9: BD 8C 27
64DC: 01 17
64DE: 02 58
64E0: 39         RTS 
;
;----------------------------------------;-----------------------------------------
;
64E1: BD 87 66      JSR $8766 ; SearchLinkedListForId(0x0117)
64E4: 01 17                     ;
64E6: 25 15         BCS $64FD ; if (entryFound == True)
64E8: BD 83 F6      JSR $83F6 ; {
64EB: B4                      ;     Sleep(0xB4)
64EC: BD 83 C9 JSR $83C9      ;     GetSwitchPressed(UpperLeftFlipperOpto)
64EF: 88                      ;     if (SwitchPressed == True)
64F0: 25 0B BCS $64FD         ;     {
64F2: 86 54 LDA #$54          ;        $172D = 0x54
64F4: B7 17 2D STA $172D      ; 
64F7: BD 8A 06 JSR $8A06      ;        CallFunction($9042)
64FA: 90 42 FF                ;        --> StartTestMode
64FD: 39                      ;     }  
                              ; }
                              ;
;--------------------------------;---------------------------------
```

Near as I can tell, both of the above functions have to do with each other. 
I could be way off but It appears the first function sets up a `0x0117` thingamajig which the second function looks for. 

With pinmame I noticed the code at `$64E6` which:  
* checks if C-bit is set
* will have C-bit clear if the function at `$64D9` had been done prior

If I don't hit `$64D9` before hitting `$64E1` then:  
* it seems the C-bit is clear so the `$64E1` function doesn't do anything.

Furthermore you can see in the 2nd function it:  
* does a `sleep()` 
* and then checks if the upper-left flipper button opto is closed (left cabinet flipper button pressed)
  * When the left button is pressed the bulk of the `$64E1` function is allowed to proceed. 
  * The function will put value `0x54` into ram location `$172D` 
  * and then call a function which is same code that gets hit when "Enter" coin door button is pressed to enter the test mode. 

Doesn't sound very exciting and it is not doing something correctly because the results aren't very joyful:

So here are the steps I did to:  
`16R + 1L + 13R + 1L + 12R + 1L` (calls `$64D9`)  
Then immediately after that do:  
`1R + 1L + 2R + 1L + 3R + 1L` (alls `$64E1`)  
Then immediately hold the left cabinet flipper button for several seconds.
(I'll let you try it and see what happens, it appears it only has effect during attract mode).

Lastly we have this `$646D` function.
I only annotated the first few instructions, see below:

```
;------------------------------------;--------------------------------------------
;
646D: 34 10         PSHS X      ;
646F: BD 83 F6      JSR $83F6   ; Sleep(0xB4)
6472: B4                        ;
6473: BD 83 C9                  ; GetSwitchPressed(UpperRightFlipperOpto)
6476: 86                        ; if (SwitchClosed == True)
6477: 25 33         BCS $64AC ; {
6479: BD CA 70      JSR $CA70 ;
647C: BD E2 F4      JSR $E2F4 ;
647F: BD D2 5F      JSR $D25F
6482: BD D2 73      JSR $D273
6485: 8E 64 C4      LDX #$64C4
6488: 8D 24         BSR $64AE
648A: BD D6 C0      JSR $D6C0
648D: 00 00
648F: 15 40
6491: 0C
6492: 8E 64 CF      LDX #$64CF
6495: 8D 17         BSR $64AE
6497: BD D6 C0      JSR $D6C0
649A: 00 00
649C: 15 41
649E: 1A
649F: BD 89 4D      JSR $894D
64A2: 01 28
64A4: BD E3 B6      JSR $E3B6
64A7: 78
64A8: BD 86 16      JSR $8616
64AB: 04
64AC: 35 90         PULS X,PC ; }
;
;----------------------------------------;--------------------------------------------
```

At the start of this function I see that it does a sleep and then checks if the right flipper button is pressed, so knowing that much, do the following:

`15R + 1L + 8R + 1L + 3R + 1L` (calls `$646D`)

Then immediately hold the right flipper button down.

I have no idea what the message means, maybe junk, maybe developer debugging thing. 
It is interesting that there is a lot of code that gets called when the combintation is used, 
including another function that `$64AE` which I didn't paste above, so maybe there's more going on than meets the eye.

This means the hacks I suggested earlier probably wouldn't have done much good since you 
have to hold a flipper button down after entering the special combination. Sorry for giving poor advice earlier.

This also means any of the unknown easter egg combinations that I've listed for other games might just need a button 
to be held down after entering the combination in order to see any effect. 

And this also shows that sometimes two different combinations might need to be entered after each other in order to see 
an effect (along with holding a button down afterwards).
