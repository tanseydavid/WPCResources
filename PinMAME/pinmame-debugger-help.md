PinMAME Debugger Help
=====================


Command Line window 
-------------------------------------

| Key             | Function Purpose                                                    |
|:----------------|---------------------------------------------------------------------|
| <kbd>UP</kbd> | Move cursor up in disassembly window
| <kbd>DOWN</kbd> | Move cursor down in disassembly window
| <kbd>PGUP</kbd> | Move cursor up one page in disassembly window
| <kbd>PGDN</kbd> | Move cursor down one page in disassembly window
| <kbd>HOME</kbd> | Move cursor to first page in disassembly window
| <kbd>END</kbd> | Move cursor to last page in disassembly window
| <kbd>LEFT</kbd> | Back to the previous point in 'follow history'
| <kbd>RIGHT</kbd> | Follow the current instruction's code or data reference

| Key             | Function Purpose                                                    |
|:----------------|---------------------------------------------------------------------|
| <kbd>TAB</kbd>  | Switch between windows (backwards SHIFT+TAB) |
| <kbd>F1</kbd>   | Help - maybe you realized this ;) |
| <kbd>F6</kbd>   | Set the focus to the next (not ignored) CPU |
| <kbd>F8</kbd>   | Step one instruction |
| <kbd>F9</kbd>   | Animate (trace) at speed set by last \"A\" command |
| <kbd>F10</kbd>  | Step over instruction at cursor (ie. execute call, jsr or bsr) |
| <kbd>F12</kbd>  | Go! |
| <kbd>ESC</kbd>  | Go! |
| <kbd>ENTER</kbd> | |
| <kbd>SHIFT+ENTER</kbd> | Like <kbd>F10</kbd>, but also skips loops, function calls, etc. |
	


### `A [<update>]`
Animate (trace) and update display once per frame [or every `<update>` opcodes only]

### `D <1|2> <address>`
Display memory `<1|2>` starting at `<address>`
	
### `E <1|2> [<address>]`
Edit memory window <1|2> [at <address>]

### `M <1|2> [BYTE|WORD|DWORD]`
Change memory window mode to default [to `BYTE|WORD|DWORD` (or `0|1|2`)]

### `F`
Fast

### `G [<address>]`
Go [and break at `<address>`]

### `J <address>`
Jump to `<address>` in disassembly window

### `R <register> <value>`
Replace `<register>` with `<value>` (`<value>` may also be a `<register>`)

### `BP  BPX <address> [<times>]`
Break on execution of `<address>` [after ignoring it `<times>`]

### `BC`
Clear execution breakpoint

### `RP <register> [<value> [<mask>]]`
Break if `<register>` changes [to `<value>` [compare after applying `<mask>`]]

### `RC`
Clear register watchpoint

### `WP  BPW <address> [<value>]`
Break if data at `<address>` changes [to `<value>`]

### `WC`
Clear data watchpoint

### `BPR <start> [<end>]`
Break if data between <start> and <end> is read or written

### `HERE`
Run to cursor

### `DASM <filename> <start> <end> [<boolean>]`
Disassemble to `<filename>` from address `<start>` to `<end>`
Opcode dump on by default [`OFF|NO|0` without]

### `DUMP <filename> <start> <end> [<data size> [<ASCII mode> [<prog/data memory>]]]`
Dump to `<filename>` from address `<start>` to `<end>` [data size `BYTE|WORD|DWORD` (also `0|1|2`)] [`ASCII` mode `OFF|TRANSLATE|FULL`  (also `0|1|2`)] [`PROG` or `DATA` memory (also `0|1`) for CPUs supporting it]

### `TRACE {<filename> [<reg1> [<reg2>...]]}|OFF`
Trace to `<filename>` [dumping `<reg1>` [`<reg2>`...]] | `OFF` to stop tracing.

### `CODELIST [filename]|OFF`
Collect code addresses during execution and condense them to blocks.
Code blocks data is written to `<filename>` when switched off

### `SAVE <filename> <start> <end> [OPCODES|DATA]`
Save binary to `<filename>` from address `<start>` to `<end>`
[either `OPCODES` (from OP_ROM, default) or `DATA` (from OP_RAM), also `0|1`].

### SCANLINE     
Toggles the display of scanlines

### SD     
Disables Sound when debugger window is active

### SE     
Enables Sound when debugger window is active

### IGNORE <cpunum>
Ignore CPU #<cpunum> while debugging or tracing

### OBSERVE <cpunum>
Observe CPU #<cpunum> while debugging or tracing

### REPEAT rate
Set keyboard initial repeat rate (rate/frame will increase to 1/frame)

### CASE DEFAULT|LOWER|UPPER (also 0|1|2)
Set disassembly case style.

### OPCODES <boolean>
Display opcodes in disassembly window

### RELATIVE <boolean>
Display relative jump addresses in disassembly window

### SQUEEZE <boolean>
Allow squeezed memory display

### COLOR <element> <foreground> [<background>]
Set <element> color to <foreground> on BLACK [or <background>].
For a list of <elements> and <colors> see mamedbg.cfg


CPU Registers Windows Help
-------------------------------------
| Key             | Function Purpose                                                    |
|:----------------|---------------------------------------------------------------------|
| <kbd>TAB</kbd>  | Switch between windows (backwards SHIFT+TAB) |
| <kbd>F1</kbd>   | Help - maybe you realized this ;) |
| <kbd>F6</kbd>   | Set the focus to the next (not ignored) CPU |
| <kbd>F8</kbd>   | Step one instruction |
| <kbd>F9</kbd>   | Animate (trace) at speed set by last \"A\" command |
| <kbd>F10</kbd>  | Step over instruction at cursor (ie. execute call, jsr or bsr) |
| <kbd>F12</kbd>  | Go! |
| <kbd>ESC</kbd>  | Go! |
| <kbd>ENTER</kbd> | |
| <kbd>SHIFT+ENTER</kbd> | Like <kbd>F10</kbd>, but also skips loops, function calls, etc. |


Disassembly Window Help
-------------------------------------

| Key             | Function Purpose                                                    |
|:----------------|---------------------------------------------------------------------|
| <kbd>D</kbd> | Change disassembly case style to default
| <kbd>L</kbd> | Change disassembly case style to lower case
| <kbd>U</kbd> | Change disassembly case style to upper case
| <kbd>M</kbd> | Toggle disassembly opcode display mode
| <kbd>UP</kbd> | Move cursor up in disassembly window
| <kbd>DOWN</kbd> | Move cursor down in disassembly window
| <kbd>PGUP</kbd> | Move cursor up one page in disassembly window
| <kbd>PGDN</kbd> | Move cursor down one page in disassembly window
| <kbd>HOME</kbd> | Move cursor to first page in disassembly window
| <kbd>END</kbd> | Move cursor to last page in disassembly window
| <kbd>LEFT</kbd> | Back to the previous point in 'follow history'
| <kbd>RIGHT</kbd> | Follow the current instruction's code or data reference

| Key             | Function Purpose                                                    |
|:----------------|---------------------------------------------------------------------|
| <kbd>TAB</kbd>  | Switch between windows (backwards SHIFT+TAB) |
| <kbd>F1</kbd>   | Help - maybe you realized this ;) |
| <kbd>F6</kbd>   | Set the focus to the next (not ignored) CPU |
| <kbd>F8</kbd>   | Step one instruction |
| <kbd>F9</kbd>   | Animate (trace) at speed set by last \"A\" command |
| <kbd>F10</kbd>  | Step over instruction at cursor (ie. execute call, jsr or bsr) |
| <kbd>F12</kbd>  | Go! |
| <kbd>ESC</kbd>  | Go! |
| <kbd>ENTER</kbd> | |
| <kbd>SHIFT+ENTER</kbd> | Like <kbd>F10</kbd>, but also skips loops, function calls, etc. |


Memory Editor Help
-------------------------------------

| Key             | Function Purpose                                                    |
|:----------------|---------------------------------------------------------------------|
| <kbd>TAB</kbd> | Switch between windows (backwards SHIFT+TAB)
| <kbd>H</kbd> | Toggle between hex, ASCII and full character set mode
| <kbd>P</kbd> | Toggle memory display between DATA and PROGRAM memory (Harvard-architecture CPUs)
| <kbd>I</kbd> | Toggle memory display between CPU internal and normal memory
| <kbd>M</kbd> | Switch memory display mode between bytes, words and dwords
| <kbd>S</kbd> | Search memory for a sequence of bytes
| <kbd>F2</kbd> | Toggle breakpoint at current cursor position
| <kbd>F4</kbd> | Run to cursor
| <kbd>F4</kbd> | Set data watchpoint to current memory location


| Key             | Function Purpose                                                    |
|:----------------|---------------------------------------------------------------------|
| <kbd>TAB</kbd>  | Switch between windows (backwards SHIFT+TAB) |
| <kbd>F1</kbd>   | Help - maybe you realized this ;) |
| <kbd>F6</kbd>   | Set the focus to the next (not ignored) CPU |
| <kbd>F8</kbd>   | Step one instruction |
| <kbd>F9</kbd>   | Animate (trace) at speed set by last \"A\" command |
| <kbd>F10</kbd>  | Step over instruction at cursor (ie. execute call, jsr or bsr) |
| <kbd>F12</kbd>  | Go! |
| <kbd>ESC</kbd>  | Go! |
| <kbd>ENTER</kbd> | |
| <kbd>SHIFT+ENTER</kbd> | Like <kbd>F10</kbd>, but also skips loops, function calls, etc. |

