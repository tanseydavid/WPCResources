WPC Orkin Errors by Number
==========================

(preliminary)

| Err # | Err # hex | Message                                       |
|-------|-----------|-----------------------------------------------|
| 1     | 0x01      | User break requested by key press
| 2     | 0x02      | Value specified for LOCKED_CMOS is not in table
| 3     | 0x03      | 6809 "reserved vector" processed
| 4     | 0x04      | swi 3 executed
| 5     | 0x05      | swi 2 executed
| 6     | 0x06      | nmi ocurred
| 7     | 0x07      | Process sleep with stack too large
| 8     | 0x08      | Couldn't allocate block for large stack!
| 9     | 0x09      | free_block called w/ Null pointer
| 10    | 0x0a      | Process not on list expected
| 11    | 0x0b      | Request to Free Ram Block failed
| 12    | 0x0c      | Exec hook called utility requiring a process id.
| 13    | 0x0d      | String too long for printf_buffer
| 14    | 0x0e      | Ill formatted % clause in printf string
| 15    | 0x0f      | Coil queue full
| 16    | 0x10      | Bad pound clause embedded in string.
| 17    | 0x11      | Message number passed is beyond table.
| 18    | 0x12      | Head or Tail of coil queue out of range
| 19    | 0x13      | GI bit from bit generator is bad
| 20    | 0x14      | Flash time of zero used.
| 21    | 0x15      | GI Number out of range.
| 22    | 0x16      | Number to lamp/flag twiddler out of range.
| 23    | 0x17      | Lamp table invalid, or not in prime real estate.
| 24    | 0x18      | Lamp string number specified is too high
| 25    | 0x19      | End Bracket while NOT in lamp string if statement.
| 26    | 0x1a      | Lamp string operator out of range
| 27    | 0x1b      | Lamp string range op got lamps in wrong order.
| 28    | 0x1c      | endif encountered before "then" on if in lamp string.
| 29    | 0x1d      | Bad matrix specified on lamp operation
| 30    | 0x1e      | get_switch_bit munged its parameters
| 31    | 0x1f      | Switch number passed to switch primitive too high
| 32    | 0x20      | Cksum init call to region that's not Prime
| 33    | 0x21      | long_binary_to_bcd passed zero length
| 34    | 0x22      | Hook (indicated by U, in apfixed) must be in prime.
| 35    | 0x23      | Special solenoid handlers not in prime real estate
| 36    | 0x24      | Score req. w/ player_up invalid, tilt, go, or diag.
| 37    | 0x25      | Product of local and global score multipliers > 255
| 38    | 0x26      | Process that just slept wrote to 1st 8 bytes of ram.
| 39    | 0x27      |  Bad score multiplier specified.
| 40    | 0x28      |  Table item out of range (beyond end of table)
| 41    | 0x29      |  Printf:  Bad character following backslash.
| 42    | 0x2a      |  Lamp routine called with lamp 0.
| 43    | 0x2b      |  Pointer for Printf won't fit in 16 bits.
| 44    | 0x2c      |  Field not in segment area
| 45    | 0x2d      |  Attempt to store bit for field, beyond last byte
| 46    | 0x2e      |  Invalid time stamp passed to clock_time_stamp
| 47    | 0x2f      |  Process with leff_number has no lamp block
| 48    | 0x30      |  Bits in LF_ and LEFL_ flags must be in same position.
| 49    | 0x31      |  LEF_FLASH_BYTES not large enought for phys. flashers
| 50    | 0x32      |  Process has P_LEFF_NUMBER w/o valid PID
| 51    | 0x33      |  Tried to allocate flasher zero for lamp effect.
| 52    | 0x34      |  Lamp effect block freed (instead of sys_leff_exit)
| 53    | 0x35      |  User field request by proc w/o that field defined.
| 54    | 0x36      |  Invalid software field number
| 55    | 0x37      |  Background display effect header invalid.
| 56    | 0x38      |  sys_deff_check called for background display effect.
| 57    | 0x39      |  Player up number invalid
| 58    | 0x3a      |  Bad or Missing Master Scroll block
| 59    | 0x3b      |  Master block required for setup or scroll operation
| 60    | 0x3c      |  Cannot locate previously setup scroll chunk
| 61    | 0x3d      |  Period or Comma 1st char, or after # (use space)
| 62    | 0x3e      |  Display scroller running with no source type set.
| 63    | 0x3f      |  No matrix bit set for lamp effect. (string specified)
| 64    | 0x40      |  Addl. lamps allocted to effect specified NEW matrix.
| 65    | 0x41      |  Software field flags need justification bits
| 66    | 0x42      |  Bad segment area specified to sys_copy_fixed_field
| 67    | 0x43      |  Dissolve requested, but background deff wasn't running
| 68    | 0x44      |  Invalid scroll chunk pointer.
| 69    | 0x45      |  Stackable effect has flag conflict (amode etc.)
| 70    | 0x46      |  Endball called from game over
| 71    | 0x47      |  Request for player area byte, out of range
| 72    | 0x48      |  Multiball device number invalid
| 73    | 0x49      |  Too many multiball devices specified
| 74    | 0x4a      |  Irq Tail hook not in prime real estate
| 75    | 0x4b      |  No processes available for ball serve
| 76    | 0x4c      |  Multiball device zero used.
| 77    | 0x4d      |  Unmonitored locked hole had a switch closure.
| 78    | 0x4e      |  Lock count on eject hole was higher than 1
| 79    | 0x4f      |  Call to trough handler for endball returned.
| 80    | 0x50      |  Call to trough handler for ball serve returned.
| 81    | 0x51      |  audit_complete called by invalid process id
| 82    | 0x52      |  Could not get process block for mulitball device kickout.
| 83    | 0x53      |  Device type number invalid for multiball device.
| 84    | 0x54      |  Ball serve condition w/ no balls in trough (you must kick one)
| 85    | 0x55      |  MULTI_ALL_BALL_CHECK called while auditing in progress
| 86    | 0x56      |  Quick leff resource req. by non-leff process
| 87    | 0x57      |  Non-display effect called sys_deff_exit
| 88    | 0x58      |  Non-lamp effect called sys_leff_exit
| 89    | 0x59      |  Effect stack pointer invalid
| 90    | 0x5a      |  Bad sound table entry, or too many sound table entries
| 91    | 0x5b      |  Bad sound script operator
| 92    | 0x5c      |  Whirl_field passed an invalid quadrant number
| 93    | 0x5d      |  Cmos ram left unprotected (sys_lock_cmos forgotten)
| 94    | 0x5e      |  HSTD Table would not initialize (Check Default Table)
| 95    | 0x5f      |  HSTD entry requested out of range
| 96    | 0x60      |  Display field too small for get_let
| 97    | 0x61      |  Internal error in GET_LET processing
| 98    | 0x62      |  Higher priority deff stopped Enter your Initials.
| 99    | 0x63      |  LARGEST_HSTD_TABLE value not large enough
| 100    |  0x64      | def_status MUST HAVE DEF_EQMAY set.
| 101    |  0x65      | Could not allocate block for test mode
| 102    |  0x66      | Audit formatting number invalid
| 103    |  0x67       | adj_name_it must specify TRUE in adj table
| 104    |  0x68       | Process dispatcher got a non-process block to dispatch
| 105    |  0x69      | Bad special help routine requested
| 106    |  0x6a      | Process executed an RTS instruction (instead of die)
| 107    |  0x6b      | Too many audits for TOTAL_AUDITS value specified.
| 108    |  0x6c      | Test report lost phasing w/ help sequencer
| 109    |  0x6d      | Too many adjustments for ADJ_TOTAL value
| 110    |  0x6e      | Exec routine called sys_get_block.
| 111    |  0x6f      | User menu descriptors out of order.
| 112    |  0x70      | Copied string too long for process block.
| 113    |  0x71      | Display Req. from display effect routine.
| 114    |  0x72      | Sleep called from EXEC routine.
| 115    |  0x73      | Switch hit reported on switch in non-scanned column.
| 116    |  0x74      | Invalid audit ram referenced.
| 117    |  0x75      | Exec level routine locked up (Detected by IRQ)
| 118    |  0x76      | ad_replay_start value is not within min/max range.
| 119    |  0x77      | Switch test could not get a ram block
| 120    |  0x78      | Ram byte ticket_to_dispense got corrupted.
| 121    |  0x79      | Units (not tens) added to score.
| 122    |  0x7a      | Current process wrote beyond its stack
| 123    |  0x7b      | Current process underflowed its stack
| 124    |  0x7c      | DMX page allocator failed
| 125    |  0x7d      | Unsupported picture format found
| 126    |  0x7e      | Vapor lock got a ball beyond the max. allowed
| 127    |  0x7f      | Vapor lock called to remove w/ 0 balls present
| 128    |  0x80      | Remove your coin switch dispatch flags (to coin_switch_handler).

