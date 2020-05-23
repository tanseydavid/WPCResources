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

```
z = decodedmximage_type1( 0x41bd, 0x20 )

//
// WPC ImageType = 01
//  Simple Repeats, Columns
//
void DMD::Decode_01(unsigned char **Source, unsigned char *Dest)
{
// IMAGE TYPE 0x04 or 0x01                ; EDF1h   Byte1 = Byte AFTER the 0x04
//
// Simple Repeats, Columns
//
// Format:
//  0x02                   Image type byte, byte that got us this far.
//   <Special Flag Byte>   Special 8-bit value that is used to signal repeats
//   <data starts here>
//
// This is a simple encoding very similar to IMAGE TYPE 0x05 or 0x02.  This
// encoding uses a simple single-special-byte at the top and whenever this
// byte is encountered, the following 2 bytes are used for Repeat/Data so that
// the Data is repeated for the number of times in 'Repeat'.
//
// The only difference between this and IMAGE TYPE 0x05 or 0x02 is that this
// encoding method writes in columns from LEFT to RIGHT starting at the top
// left and ending at the bottom right of the DMD.
//
	Decode_01or02(Source,&Dest,WRITE_TYPE_COLUMNS);
}
```
