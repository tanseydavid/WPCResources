WPC Bank Addresses
=====================================

## 6809 Address Space
The 6809 microprocessor used in the WPC platform is a 8/16 bit CPU, capable of working directly with a maximum address space of 64K.  This reflects an addressable space with a range from `$0000` through `$FFFF`.

## WPC Address Space

### Below `$4000`
* Any address reference <`$4000` is either RAM or I/O (i.e. **NOT ROM**)

In the WPC address space all addresses below `$4000` reference either RAM or I/O.  The important point here is that all addresses below `$4000` are NOT ROM addresses.  For more details about the mapping of addresses below `$4000` see (*).

### `$4000` and above
* Any address reference >=`$4000` is ROM reference

In WPC all references to addresses from `$4000` through `$FFFF` are ROM addresses but not all of the ROM is treated the same way, or as the same "type". 

Part of the ROM winds up as FIXED addresses and the rest must be accessed via BANK-SWITCHING.

#### `$4000` through `$7FFF` 
* Any address reference between `$4000` and `$7FFF` is a reference to the BANKSWITCHED portion of the ROM.  

In most cases, references to addresses in this range will also specify a Bank (via BankId) to be specific and unambiguous.  Any references to addresses in this range *without* a specific BankId implies that it refers to that address in the *current bank*.

#### `$8000` through `$FFFF`
* Any address reference >=`$8000` is ROM reference to the FIXED (sys) portion of the ROM

### WPC Bank Switching


#### Memory Addresses - WPC Bank Switching

| Address | Type | Description                                       | 
|---------|------|---------------------------------------------------| 
| `$0011` | RAM  | current bank selection                            |  
| `$3ffc` | I/O  | bank selector port                                | 
| `$4000` | ROM  | every ROM bank has an ID marker in the first byte | 



## WPC MAME-Debugger Commands 
### Break on WPC Bank Address 

```
Bank Address: $68a0
BankId: $35

rp {PC==0x68a0 && b@4000==0x35}

```

