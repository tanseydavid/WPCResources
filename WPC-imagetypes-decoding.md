WPC DMX ImageTypes and Decoding
-------------------------------

```
case 0x00	:  //  Raw 32 bytes by 16 byes copy, no encodings.
	Decode_00(Source, Dest);

case 0x01   :  //  Simple Repeats, Columns
	Decode_01(Source, Dest);

case 0x02   :  //  Simple Repeats, Rows
	Decode_02(Source, Dest);

case 0x03   :  //  <unsure>
	Decode_03(Source, Dest);
	return PLANE_STATUS_UNIMPLEMENTED_TYPE; // this is a cheat but we know that type 03 is not being decoded

case 0x04   :  //  Complex Repeats, 9-byte header, Columns
	Decode_04(Source, Dest);

case 0x05   :  //  Complex Repeats, 9-byte header, Rows
	Decode_05(Source, Dest);

case 0x06   :  //  XOR-Repeat, Columns
	Decode_06(Source, Dest, XorFlags, XorBits);

case 0x07   :  //  XOR-Repeat, Rows
	Decode_07(Source, Dest, XorFlags, XorBits);

case 0x08   :  //  Bulk Skips and Bulk Repeats, Columns
	Decode_08(Source, Dest, Skipped);

case 0x09   :  //  Bulk Skips and Bulk Repeats, Rows
	Decode_09(Source, Dest, Skipped);

case 0x0A   :  //  Write Data Bytes or Multiple Skips, Columns
	Decode_0A(Source, Dest, Skipped);

case 0x0B   :  //  Write Data Bytes or Multiple Skips, Rows
	Decode_0B(Source, Dest, Skipped);

default	:
	TmpStr.Format("Unknown Image Type 0x%02x",ch);
```
