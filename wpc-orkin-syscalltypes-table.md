WPC Orkin SysCallTypes table
============================

GW_PC Bank $20
--------------
```
;---------------------------------------------------------
tblOrkinSysCallTypes:
;
; 5 bytes per entry
; 	2 bytes rangeStart
;   2 bytes rangeEnd
;   1 byte CallType
;---------------------------------------------------------
tblSysCallRangeTypes:
;---------------------------------------------------------
; entry 0x0 (dec: 0) 
420E: 82 6c 85 fa   	; $826c - $85fa 
4212: 04  				; type = 4 
;
; entry 0x1 (dec: 1)
4213: 85 fa 88 cf		; $85fa - $88cf
4217: 05  				; type = 5
;
; entry 0x2 (dec: 2)
4218: 88 cf 8a75   		; $88cf - $8a75
421c: 06       			; type = 6
;
; entry 0x3 (dec: 3)
421D: 8a 75 8b 18    	; $8a75 - $8b18
4221: 07       			; type = 7
;
; entry 0x4 (dec: 4)
4222: 8b 18 8c 18  		; $8b18 - $8c18
4226: 08  				; type = 8
;
; entry 0x5 (dec: 5)
4227: 8c 18 8c 64		; $8c18 - $8c64
422b: 09 				; type = 9
;
;
;-----------------------------------------------------
GetSysCallType:
;
;-----------------------------------------------------
422C: 86 01              LDA   #$01		; TYPE = 1
422E: 8c 88 cf           CMPX  #$88cf	; does X = JSR_BANK()
4231: 27 0f		 BEQ   :exit	; yes, exit with TYPE = 1
; 
4233: 86 02              LDA   #$02   	; TYPE = 2
4235: 8c 85 fa           CMPX  #$85FA	; does X = JSR_BANK_ADDRESS_AT()
4238: 27 08              BEQ   :exit	; yes, exit with TYPE = 2
;
423A: 86 03              LDA   #$03		; TYPE = 3
423C: 8c 89 0a           CMPX  #$890A	; does X = JMP_BANK() 
423F: 27 01              BEQ   :exit	; yes, exit with TYPE = 3
;
4241: 4f                 CLRA  			; TYPE = 0 (address not known)
:exit
4242: 39                 RTS   
; 
```



ADDAM_L5 Bank $20
------------------

```
--------------------------------
ADDAM_L5.ROM
--------------------------------
$829B - $8653  TYPE = 04 
$8653 - $8927  TYPE = 05 
$8927 - $8ACC  TYPE = 06 
$8ACC - $8BA8  TYPE = 07 
$8BA8 - $8CA8  TYPE = 08 
$8CA8 - $8CF4  TYPE = 09


	86 01 			TYPE = 1
	8C 89 27 		applies only to $8927 - JSR_BANK() 
	27 0F 
	86 02 			TYPE = 2
	8C 86 53 		applies only to $8653 - JSR_BANK_ADDRESS_AT()
	27 08 
	86 03 			TYPE = 3
	8C 89 61 		applies only to $8961 - JMP_BANK()
	27 01 
	4F 				TYPE = 0 (not known)
	39
	

```