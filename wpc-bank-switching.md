WPC Bank Addressing
===================

### $4000 - $7FFF the paged BANK region
* 16K in length
* Banks (a.k.a. Pages)
* BankId Marker byte 
    * first byte of every BANK `$4000` contains the BankId value (i.e. marker) for that bank  
    * vs `$3FFC - WPC_ROM_BANK` 
    * vs `$0011 ramCurrentBankId`
* Bank Address references
    * Address references (JSR routines or data) in the range `$4000-$7FFF` usually need an additional byte for BankId (total of 3 bytes).
	* 3 byte bank address examples
		* JSR_BANK()
		* Bank Address tables

### $8000 - $FFFF the fixed SYS region
* The region is 32K in length and is always located at the end of the space ROM
* I refer to addresses in this range as SYS addresses
* This address range may be what Orkin messages refer to as "Prime Real Estate"
* 3 byte Bank Addresses 
	* 2 byte JMP/JSR or pointer address followed by 1 byte Bank Id
	* sometime a table of Bank Addresses will have jump addresses that are from the SYS area
		* these Bank Address entries will have a BankId value of `$FF`
* The 32KB in the fixed SYS region has a BankId marker at $8000, the first byte of address region, 
	typically marked with ID 0x3E (although in tables of bank addresses, this region is usually referred to as BankId 0xFF)

	
```	
save[{d|i}] <filename>,<address>,<length>[,<cpu>]

	save gw_adjustments_factory_reset.mem, 0x1b1d, 0xba, 0
	save gw_adjustments_serial.mem, 0x1b1d, 0xba, 0

	load gw_adjustments_serial.mem, 0x1b1d, 0xba, 0

	dump gw_adjustments_factory_reset.dmp, 0x1b1d, 0xba, 0, 0

suspend 0;b!037b=1;pc=8eb4;bp 410a;resume 0;b=0x20;g

b!037b=1;pc=8eb4;bp 410a;b=0x20;
wpset 3e66,2,rw,1,{g;};wpset 3d60,2,rw,1,{g;};
b!037b=1;pc=8eb4;bp 410a;b=0x1;g


OrkinCallIndexInA
b!037b=1;pc=8eb8;bp 410a;a=0x1;g


OrkinCallIndexInA = 10 needs X = ?
b!037b=1;pc=8eb8;bp 4435;a=0x10;x=0x0B11;g
```

GW_PC 
======

### Calls to `JSR_BANK_ADDRESS_AT()`

```
JSR_BANK_ADDRESS_AT( $047c )

JSR_BANK_ADDRESS_AT( $8001 ) 	8001: $478c, $30  
JSR_BANK_ADDRESS_AT( $8004 )	8004: $4795, $30
JSR_BANK_ADDRESS_AT( $8007 )	8007: $735c, $3d

JSR_BANK_ADDRESS_AT( $801f )	801F: $752e, $3d

JSR_BANK_ADDRESS_AT( $8022 )	8022: $40db, $30
JSR_BANK_ADDRESS_AT( $8025 )	8025: $4762, $30
JSR_BANK_ADDRESS_AT( $8028 )	8028: $4945, $30

JSR_BANK_ADDRESS_AT( $8034 )	8034: $47e7, $30
JSR_BANK_ADDRESS_AT( $8037 )	8037: $7530, $3d

JSR_BANK_ADDRESS_AT( $8091 )	8091: $7561, $3d


JSR_BANK_ADDRESS_AT( $80af )	80AF: $7596, $3d

JSR_BANK_ADDRESS_AT( $80b2 )	80B2: $7597, $3d

JSR_BANK_ADDRESS_AT( $80c1 )	80C1: $498b, $30

JSR_BANK_ADDRESS_AT( $80dc )	80DC: $75a1, $3d

JSR_BANK_ADDRESS_AT( $80e8 )	80E8: $e9f7, $ff
JSR_BANK_ADDRESS_AT( $80ee )	80EE: $75a4, $3d

JSR_BANK_ADDRESS_AT( $80f1 )	80F1: $75a5, $3d

JSR_BANK_ADDRESS_AT( $80fd )	80FD: $75a9, $3d

JSR_BANK_ADDRESS_AT( $8106 )	8106: $e685, $ff
```

### Orkin Subroutines with series parameters calls

`$4980, $20` gets called with `B =`
* 0x00	 0  
* 0x08	 8  
* 0x10	16  
* 0x18	24  
* 0x20	32  
* 0x28	40  
* 0x40	64  
* 0x30	48  
* 0x38	56  


`$4A01, $20`  gets called with `X =`

```
X=#$0100	256
				+96
X=#$0160	352
				+96
X=#$01c0	448
				+96
X=#$0220	544
```
 
`$4EFA, $20`  gets called with `X =`

```
X=#$0100	256
				+96
X=#$0160	352
				+96
X=#$01C0	448
				+96
X=#$0220	544
```


### DASM WPC notes 

```
const dasm = require('../../test/tracer/dasm-entry');
const dasmEntriesWpc = require('./wpc-dasm-entries');
```

    dasmEntries.add( 0x85EA, 1 );
    dasmEntries.add( 0xB645, 0, 'CheckBallInPlayIsLastBall');
    
    dasmEntries.addTable( 0x4000, 0x20, 'pageMarker_bnk_20', 1, 1 );
    dasmEntries.addTableStrings( 0x439f, 0x20, 'tblStrings-FreeList', 0x0e );
    dasmEntries.addTableWpc( 0x57db, 0x20, 'tblWpcTwoBytes' );
    dasmEntries.addTableSys( 0xFFBE, 'vectors', 33, 2 );

    dasmEntries.add( 0x85fa, 2, 
        'JSR_BANK_ADDRESS_AT', [ 3 ],                      dasm.printMacroInstruction_JSR_BANK_ADDRESS_AT);

    dasmEntries.add( 0x88CF, 3,
        'JSR_BANK',
        [ 2, 1 ],
        dasm.getMacroInstruction_JSR_BANK );         // printInstruction_JSR_BANK(pc, instr, line);

    dasmEntries.addSysMacro( 0xf88a, 3, [2, 1] );
    