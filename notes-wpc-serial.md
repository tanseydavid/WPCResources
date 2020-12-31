Notes - WPC Serial Support
==========================

> Each NULL modem has built-in support for the 'bitbanger' and dies translation between the stream and the selected baudrate

> NULL modem "bitbanger" accepts a socket address as an argument


```
ASCII   5  0x05  <CTRL-E>   ENQ  
ASCII  13  0c0D  <CTRL-M>   CR
ASCII  17  0x11  <CTRL-Q> 	XON   DC1  
ASCII  19  0x13  <CTRL-S>	  XOFF  DC3  
```
