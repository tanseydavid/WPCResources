Things + Nouns WPC/Orkin
==============================================================================

	* Audits
	* Adjustments
	* Game
	* Lamps / Lamp Effects / Lamp Block
	* GI
	* Coils / Coil Queue / Special Solenoid Handlers
	* Switches
	* Ball Handling
	* Multiball / DEVICES
	* Display / Display Effects
	* Processes
	* Sound
	* String handling
	* Tables / Software fields
	* APPLE / Orkin
	* System
	* CPU
	* Memory
	
	
AUDITS
--------------------------------------------------------------------
* Audit formatting number invalid
* Too many audits for TOTAL_AUDITS value specified.
* Test report lost phasing w/ help sequencer

ADJUSTMENTS
--------------------------------------------------------------------
* Too many adjustments for ADJ_TOTAL value
* ad_replay_start value is not within min/max range.
* adj_name_it must specify TRUE in adj table

GAME
--------------------------------------------------------------
* Player up number invalid
* Units (not tens) added to score.
* Score req. w/ player_up invalid, tilt, go, or diag.
* Product of local and global score multipliers > 255
* Bad score multiplier specified.
* Endball called from game over
* HSTD Table would not initialize (Check Default Table)
* HSTD entry requested out of range
* LARGEST_HSTD_TABLE value not large enough

## LAMPS / LAMP EFFECTS (leff)

#### Physical lamps / Logical lamps
* Lamp numbers are 1-relative

#### Lamp Table (must be in PRIME-RealEstate)

#### Lamp Operation matrix

#### Lamp routines

#### Lamp effect list

#### Lamp blocks / Lamp effect blocks

#### Lamp Effects vs. non-Lamp Effects
* Lamp Effects matrix-bits

#### Lamp Strings
*  Lamp String number
* can have IF, THEN and ENDIF constructs
* Lamp String operators
* Lamp String range operator

####  Additional lamps can be allocated to effect

	* lamp/flag twiddler (number-to-lamp-flag-twiddler)
	* LF_ flags / LEFL_ flags
	* Flasher numbers are 1-relative

#### Orkin Messages - Lamp-related 
* Lamp table invalid, or not in prime real estate.
* Lamp string operator out of range
* Lamp string range op got lamps in wrong order.
* endif encountered before "then" on if in lamp string.
* End Bracket while NOT in lamp string if statement.
* Number to lamp/flag twiddler out of range.
* Lamp string number specified is too high
* Lamp routine called with lamp 0.
* Bad matrix specified on lamp operation
* Non-lamp effect called `sys_leff_exit`
* Lamp effect block freed (instead of `sys_leff_exit`)
* Non-lamp effect called `sys_leff_exit`
* No matrix bit set for lamp effect. (string specified)
* Addl. lamps allocted to effect specified NEW matrix.
* Quick leff resource req. by non-leff process
* Process has P_LEFF_NUMBER w/o valid PID
* Process with leff_number has no lamp block
* Bits in LF_ and LEFL_ flags must be in same position.
* Matrix shown in lamps. Press any key to continue.
* Tried to allocate flasher zero for lamp effect.
* Lamp Effect Block
* ---- ------ -----
* Lamp Effect Block
* Lamp effect List:
* LEF 
* LEFF-(
* Physical Lamps:
* Logical Lamps:
* Returned Leff
* -------- ----


GI
-----------------------------------------------------------
	* GI bit
	* bit generator
	* Flash time (must be > 0)
	* GI number
	* LEF_FLASH_BYTES (must be large enough for physical flashers)
	
* GI bit from bit generator is bad
* Flash time of zero used.
* GI Number out of range.
* LEF_FLASH_BYTES not large enought for phys. flashers


COILS / COIL QUEUE
------------------------------------------------------------------------------
	* Coil Queue
	* Special Solenoid Handlers

* Coil queue full
* Head or Tail of coil queue out of range
* Special solenoid handlers not in prime real estate
	
SWITCHES
------------------------------------------------------------------------------
	* Switch hits
	* Scanned column / non-scanned column
	* Switch number / switch primitive
	* get_switch_bit
	* coin switch dispatch flags
	* coin_switch_handler
	* Hook / U / apfixed
	* Vapor lock / max balls allowed
	* Vapor lock 'remove' must have > 0 balls present
	* Physical switch state / logical switch state
	
* Switch hit reported on switch in non-scanned column.
* Switch number passed to switch primitive too high
* `get_switch_bit` munged its parameters
* Remove your coin switch dispatch flags (to `coin_switch_handler`).
* Hook (indicated by U, in `apfixed`) must be in prime.
* Vapor lock got a ball beyond the max. allowed
* Vapor lock called to remove w/ 0 balls present
* Physical state of switches:
* Logical state of switches:
* S_GS
* S_TILT
* S_EB
* W_EB
* S_BS

BALL HANDLING
--------------------------------------------------------------------------------
	* Trough Handler
	* Trough Handler endball routine
	* Trough Handler ball serve routine / requires a process
	* Ball serve condition
	* No balls in trough condition
	
* Ball serve condition w/ no balls in trough (you must kick one)
* Call to trough handler for endball returned.
* Call to trough handler for ball serve returned.
* No processes available for ball serve


MULTIBALL / DEVICES
------------------------------------------------------------------------------
	* Monitored / Unmonitored locked hole
	* Multiball device #
	* Number of multiball devices / 1-relative
	* "Device Type Number" / multiball-device-type
	* Lock counts
	* "Multiball device kickout" has a PROCESS BLOCK
	* MULTI_ALL_BALL_CHECK / cannot be called while auditing in progress
	
* Multiball device number invalid
* Too many multiball devices specified
* Multiball device zero used.
* Device type number invalid for multiball device.
* Unmonitored locked hole had a switch closure.
* Lock count on eject hole was higher than 1
* Could not get process block for mulitball device kickout.
* `MULTI_ALL_BALL_CHECK` called while auditing in progress

DISPLAY / DISPLAY EFFECTS (deff)
--------------------------------------------------------------
	* Display Effects (deff) / Non-display effects
	* "bad segment area"
	* Background display effect / Background display effect header
	* Dissolve
	* Enter your Initials display effect
	* Display effect priorities
	* Scrollblock / Master-Scrollblock
	* Setup operation
	* Scroll operation
	* Scroll chunk / Scroll chunk pointer
	* Display scroller / Display scroller sourcetype
	* display effect routines
	* DMX page allocator
	* supported / unsupported picture formats
	* Effect Stack / Effect Stack Pointer
	* display "Segment area"
	* Known / unknown segment
	
* Non-display effect called `sys_deff_exit`
* Bad segment area specified to `sys_copy_fixed_field`
* Background display effect header invalid.
* `sys_deff_check` called for background display effect.
* Dissolve requested, but background deff wasn't running
* Higher priority deff stopped Enter your Initials.
* Bad or Missing Master Scroll block
* Master block required for setup or scroll operation
* Cannot locate previously setup scroll chunk
* Display scroller running with no source type set.
* Invalid scroll chunk pointer.
* Display Req. from display effect routine.
* DMX page allocator failed
* Unsupported picture format found
* Effect stack pointer invalid
* Segment area (0x%pxy) in displays.
* Unknown seg. addr=%pxy
* DFF_LEFT, DFF_RIGHT, DFF_SEVEN_SEGS
* p1seg1, p2seg1, p3seg1, p4seg1
* p1seg2, p2seg2, p3seg2, p4seg2
* p1seg3, p2seg3, p3seg3, p4seg3
* p1seg4, p2seg4, p3seg4, p4seg4
* Character String
* --------- ------
* Display Scroll Slave Block
* ------- ------ ----- -----
* Scroll Chunk
* ------ -----
* Display Scroll Master Block
* ------- ------ ------ -----

PROCESSES
------------------------------------------------------------------------------
Process Block
------- -----
	* Process Block / non-Process Block
	* Process Block Address
	* Process ID (aka PID, Proc id)
	* `sys_suicide` (can be called by a process)
	* Process can 'sleep'
	* Process can be 'killed'
	* Process can be 'on-a-list'
	* `audit_complete` (can be called by a process)
	* can have a priority
	* can have a P_LEFF_NUMBER
	* can have a leff_number
	* can have a lamp block
	* Process dispatcher
	* Process 'stack' (overflow / underflow)
	* "1st 8 bytes of RAM"
	* Slept process should not write to 1st 8 bytes of RAM
	* Process calls "DIE" rather than RTS
	* Process can be on FREE list / REGULAR list / PRIORITY list
	
* ** Not a process block address. **
* Proc id=%xy called sys_suicide.
* Proc id=%xy killed.
* Current process wrote beyond its stack
* Current process underflowed its stack
* Process dispatcher got a non-process block to dispatch
* Process sleep with stack too large
* Process not on list expected
* Process that just slept wrote to 1st 8 bytes of ram.
* Process executed an RTS instruction (instead of die)
* %pxy ON FREE LIST! (called suicide)
* audit_complete called by invalid process id

* !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
* Priority List:
* Regular Process List:
* 
*   Addr  PC    PG  ID    Time  A   B   X     Y     U     Ram   Aux   Leff
* !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

* Local Flags, Global Flags

* Free list:
* "McAddr" 
* PC, PG, ID  
* "MlTime
* "McAddr
* !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
* PID, Num, Pri, Flg, GI, FLS1, FLS2, Lp12, Lp34, Lp56, Lp78
* !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
* "McAddr
* 
* !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
* Next, PID, Num, Pri, Flg, GI, FLS1, FLS2, FLS3, Lamp, 
* !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
* "McAddr
* 
* Next, Rate, Left

SOUND
--------------------------------------------------------------------
	* Sound Table
	* Sound script / Sound script operators

* Bad sound table entry, or too many sound table entries
* Bad sound script operator


STRING HANDLING
--------------------------------------------------------------------
	* % formatting / # clause / backslash escaping
	* Message number
	* Message Table
	* String too long for Process Block
	
* String too long for `printf_buffer`
* Ill formatted % clause in `printf` string
* Bad pound clause embedded in string.
* Message number passed is beyond table.
* Printf:  Bad character following backslash.
* Pointer for Printf won't fit in 16 bits.
* Period or Comma 1st char, or after # (use space)
* Copied string too long for process block.


TABLES / SOFTWARE FIELDS
--------------------------------------------------------------------
	* Software Defined Fields / Software Defined Field numbers / Software Defined Field flags / Software Defined Field flags - justification bits
	* Table items / Table item numbers
	* User fields (can be requested by Processes)
	* Field in segment area / field not in segment area
	* Display fields / display field sizes (get_let / GET_LET)
	
* Table item out of range (beyond end of table)
* Invalid software field number
* User field request by proc w/o that field defined.
* Field not in segment area
* Display field too small for `get_let`
* Internal error in `GET_LET` processing
* Attempt to store bit for field, beyond last byte
* Software field flags need justification bits
* Software Defined Fields
* -------- ------- ------
* 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F


APPLE / ORKIN
--------------------------------------------------------------------
	* Test Mode
	* APPLE errors, FATAL and NON-FATAL 
	* User-Defined errors, FATAL and NON-FATAL 
	* User BREAK request
	
* Apple: unimplemented code %a
* Apple: invalid code %a from Orkin.
* Could not allocate block for test mode
* ** User Abort **
* ** USER DEFINED ERROR 0x%r2zxa (FATAL) **
* ** USER DEFINED ERROR 0x%r2zxa (NON-FATAL) **
* ** APPLE ERROR 0x%r2xza (FATAL) **
* ** APPLE ERROR 0x%r2xza (NON-FATAL) **
* Error: negative stack!
* Error not known by debugger.
* User break requested by key press


SYS
--------------------------------------------------------------------
	* cksum_init
	* User Menu descriptors
	* `long_binary_to_bcd` / length parameter must be > 0
	* `clock_time_stamp`
	* Special Help routines
	* Whirl_field / valid quadrant numbers / invalid quadrant numbers
	* `def_status`
	* `DEF_EQMAY`
	* `Sleep`
	* `sys_get_block`
	* EXEC-level routines
	* EXEC hooks
	* UTILITY requiring process IDs
	* `ticket_to_dispense` (this is a RAM byte)
	* Stackable effects / Stackable effect flags / Stackable effect flag conflicts (amode etc.)
	* Stackable effect flag = "amode"
	* Block types
	* Aux stack
	* switch_alarm_counters / bad or max counts

	
* Cksum init call to region that's not Prime
* User menu descriptors out of order.
* `long_binary_to_bcd` passed zero length
* Invalid time stamp passed to `clock_time_stamp`
* Bad special help routine requested
* `Whirl_field` passed an invalid quadrant number
* def_status MUST HAVE DEF_EQMAY set.
* `Sleep` called from EXEC routine.
* Exec routine called `sys_get_block`.
* Exec level routine locked up (Detected by IRQ)
* Exec hook called utility requiring a process id.
* Ram byte `ticket_to_dispense` got corrupted.

* Stackable effect has flag conflict (amode etc.)

* Carry Seg, Carry Dim
*   Addr  PID   #   Pri Flg GI  FLSH1 FL2 Lp12  Lp34  Lp56  Lp78
* ** Block type %a **
*   ----- ---- --
* User Allocated
* ---- ---------
* Aux Stack
* --- -----
* Blocks = %a,   Free = %y,   
* Min. Free = %u
* Counts till bad/max counts, switch_alarm_counters at 

*        D1    C1    C2    C3    C4    C5    C6    C7    C8


CPU
--------------------------------------------------------------------
	* IRQ Tail hook
	* CMOS RAM protected or unprotected / `sys_lock_cmos`
	* LOCKED_CMOS value (should be in table)
	
* Irq Tail hook not in prime real estate
* Cmos ram left unprotected (`sys_lock_cmos` forgotten)
* Value specified for `LOCKED_CMOS` is not in table
* 6809 "reserved vector" processed
* swi 3 executed
* swi 2 executed
* nmi ocurred


MEMORY
--------------------------------------------------------------------
	* Player area byte(s)
	* Audit ram / invalid audit ram
	* Large stack / block for large stack
	* free_block / Free Ram Block
	* Switch Test
	
* Invalid audit ram referenced.
* Couldn't allocate block for large stack!
* `free_block` called w/ Null pointer
* Request to Free Ram Block failed
* Switch test could not get a ram block
* Request for player area byte, out of range

FUNCTIONS REFERENCED
--------------------------------------------------------------------
* `sys_leff_exit`
* `sys_deff_exit`
* `sys_deff_check`
* `sys_copy_fixed_field`
* `sys_suicide`
* `sys_get_block`
* `sys_lock_cmos`
* `get_switch_bit`
* `coin_switch_handler`
* `audit_complete`
* `long_binary_to_bcd`
* `clock_time_stamp`

OTHER NAMED REFERENCES
--------------------------------------------------------------------
* `TOTAL_AUDITS`
* `ADJ_TOTAL`
* `ad_replay_start`
* `adj_name_it`
* `player_up`
* `LARGEST_HSTD_TABLE`
* `P_LEFF_NUMBER` ("process" lamp effect number)
* `LF_` and `LEFL_` flags
* `LEF_FLASH_BYTES`
* `WHOLE`, `EQMAY`, `SPEC`, `DEAD`, `EXCL`, `UNUSED`
* `SYNCHRO`
* `PAUS`, `TICKS`, `RIGHT`, `STRING`, `FIELD`, `CONST`, `CARRY`, `SEVEN`
* `Whirl_field`
* `def_status` (= `DEF_EQMAY`)
* `ticket_to_dispense` (`RAM BYTE`)
