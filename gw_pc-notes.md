gw_pc
======

Orkin SysCall Types + Inline Parameter counts
---------------------------------------------

* 61   - 1 inline parameter byte  
* 47   - 2 inline parameter bytes  
* 11   - 3 inline parameter bytes  
* 9   - 4 inline parameter bytes  
* 7   - 5 inline parameter bytes  
* 3   - 6 inline parameter bytes  

138 total subroutines with inline parameters


### MAME debugger to save and restore Adjustments in `gw_pc`

```	
save[{d|i}] <filename>,<address>,<length>[,<cpu>]

	save gw_adjustments_factory_reset.mem, 0x1b1d, 0xba, 0
	save gw_adjustments_serial.mem, 0x1b1d, 0xba, 0

	load gw_adjustments_serial.mem, 0x1b1d, 0xba, 0

	dump gw_adjustments_factory_reset.dmp, 0x1b1d, 0xba, 0, 0
```

### MAME debugger to force LINKED GAME in `nbaf_31`

```
suspend 0;b!037b=1;pc=8eb4;bp 410a;resume 0;b=0x20;g

b!037b=1;pc=8eb4;bp 410a;b=0x20;
wpset 3e66,2,rw,1,{g;};wpset 3d60,2,rw,1,{g;};
b!037b=1;pc=8eb4;bp 410a;b=0x1;g


OrkinCallIndexInA
b!037b=1;pc=8eb8;bp 410a;a=0x1;g


OrkinCallIndexInA = 10 needs X = ?
b!037b=1;pc=8eb8;bp 4435;a=0x10;x=0x0B11;g
```

## WPC MAME-Debugger Commands 
### Break on WPC Bank Address 

```
Bank Address: $68a0
BankId: $35

rp {PC==0x68a0 && b@4000==0x35}

```

