WPC Serial Output and Config notes
==================================

```
// TESTING ns16550
NS16550(config, m_uart, UART_CLK );
// TESTING ns16550
```

```
ins8250_device &uart0(INS8250(config, "uart_0", XTAL(1'843'200)));
```

### WPC_SERIAL_CTRL Bytes WRITE 

| Hex   | decimal | ASCII | binary     |
|-------|---------|-------|------------|
| 0x00	| 0	 	  | nul	  | 0000 0000  |
| 0x40  | 64	  | @	  | 0100 0000  |
| 0x4e  | 78	  | N	  | 0100 1110  |
| 0x25  | 37	  | %	  | 0010 0101  |

### WPC_SERIAL_CTRL Bytes READ 

| Hex   | decimal | ASCII | binary     |
|-------|---------|-------|------------|
| 0x21 	| 33 	  | !     |	0010 0001  | 
| 0x61 	| 97      | a	  | 0110 0001  |
| 0x01 	|  1 	  |      | 0000 0001  |



------------------------------------------------------------------------
```
6809 Homebrew Computer with NS16550 UART code:
https://github.com/74hc595/Ultim809/blob/master/code/rom/uart.asm
https://www.c64-wiki.com/wiki/PLA_(C64_chip)#:~:text=The%20Programmable%20Logic%20Array%20(PLA,connected%20to%20the%20data%20bus.
http://skoe.de/docs/c64-dissected/pla/c64_pla_dissected_a4ds.pdf
http://byterunner.com/16550.html
```
------------------------------------------------------------------------

```
0x00 -> FCR
0x00 -> IER == disable interrupts
0x0C -> MCR == clear modem controls, LED off
0x83 -> LCR == 8 data bits, no parity, 1 stop bit + enable divisor latch

AND 0x7F -> LCR  == disable divisor latch
```
------------------------------------------------------------------------



```
WPC_SERIAL_CTRL - READ: $60 (dec: 96 char: `)

UART-> WRITE (offset 1): $00 dec: 0 char:
UART-> WRITE (offset 1): $40 dec: 64 char: @
	UART->mcr WRITE: $40													0100 0000

UART-> WRITE (offset 1): $4e dec: 78 char: N								0100 1110
	uart-set_data_frame: startbits=1, databits=7, parity=1, stopbits=3

UART-> WRITE (offset 1): $25 dec: 37 char: %								0010 0101
	uart-set_data_frame: startbits=1, databits=8, parity=0, stopbits=1

UART-> WRITE (offset 1): $00 dec: 0 char:
UART-> WRITE (offset 1): $40 dec: 64 char: @
	UART->mcr WRITE: $40

UART-> WRITE (offset 1): $4e dec: 78 char: N
	uart-set_data_frame: startbits=1, databits=7, parity=1, stopbits=3

UART-> WRITE (offset 1): $25 dec: 37 char: %
	uart-set_data_frame: startbits=1, databits=8, parity=0, stopbits=1

WPC_SERIAL_BAUD - WRITE: 03 3 
---------------------------------------------------------------------------
uart->ier = 0x00  ( ...  ...  ...  ....  msr  lsr  thre  rxd  )
uart->lcr = 0x03  ( dlab  brk  0  0  0  stop  1  1  )
uart->lsr = 0x60  ( ...  TSRE  THRE  bu  fe  pe  oe  dr  )
uart->mcr = 0x00  (... ... ...  lpbk  out2  out1  rts  dtr  )
uart->msr = 0x11  ( cd  ri  dsr  CTS   ...   ...   ...  dCTS  )
uart->dlab = 0x000c
---------------------------------------------------------------------------

WPC_SERIAL_CTRL - READ: $61 (dec: 97 char: a)		0110 0001
WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)		0010 0001
WPC_SERIAL_CTRL - READ: $01 (dec: 1 char: )		0000 0001


WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)
WPC_SERIAL_CTRL - READ: $61 (dec: 97 char: a)
WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)
WPC_SERIAL_CTRL - READ: $61 (dec: 97 char: a)
WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)
WPC_SERIAL_CTRL - READ: $01 (dec: 1 char: )


WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)
WPC_SERIAL_CTRL - READ: $61 (dec: 97 char: a)
WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)
WPC_SERIAL_CTRL - READ: $61 (dec: 97 char: a)
WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)
WPC_SERIAL_CTRL - READ: $61 (dec: 97 char: a)
WPC_SERIAL_CTRL - READ: $21 (dec: 33 char: !)
WPC_SERIAL_CTRL - READ: $01 (dec: 1 char: )
```