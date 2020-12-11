WPC-EDIT methods
-------------------

* `DecodeVariableSizedImage`
* `DecodeVariableSizedImage_Centered`
* `DecodeVariableSizedImageIndex_NoHeader`
* `DecodeVariableSizedImageIndex_Header`
* `DecodeFullFrameGraphic`
* `DecodeImageToPlane`


[6809 SBASM](https://www.sbprojects.net/sbasm/6809.php)  
[6809 IRQs](http://www.roust-it.dk/coco/6809irq.pdf)  


```
* 00-Raw
* Simple-repeats 
	(01-cols, 02-rows)
* 03-Not Implemented
* Complex-repeats-9-byte-header 
	(04-cols, 05-rows)
* XOR-repeats 
	(06-cols, 07-rows)
* Bulk Skips + Bulk Repeats 
	(08-cols, 09-rows)
* Write Data Bytes or Multiple Skips 
	(0A-cols, 0B-rows)
```

```
--------------------------------------------
//  Raw 32 bytes by 16 bytes copy, no encodings.

Decode_00
Decode_00(Source, Dest);



--------------------------------------------
Decode_01or02( )
--------------------------------------------
//  Simple Repeats, Columns

Decode_01
Decode_01(Source, Dest);

--------------------------------------------
//  Simple Repeats, Rows

Decode_02
Decode_02(Source, Dest);



--------------------------------------------
//  <unsure>

Decode_03
Decode_03(Source, Dest);
return PLANE_STATUS_UNIMPLEMENTED_TYPE; 

// this is a cheat but we know that type 03 is not being decoded



--------------------------------------------
Decode_04or05( )
--------------------------------------------
//  Complex Repeats, 9-byte header, Columns

Decode_04
Decode_04(Source, Dest);

--------------------------------------------
//  Complex Repeats, 9-byte header, Rows

Decode_05
Decode_05(Source, Dest);



--------------------------------------------
Decode_06or07( )
--------------------------------------------
//  XOR-Repeat, Columns

Decode_06
Decode_06(Source, Dest, XorFlags, XorBits);

--------------------------------------------
//  XOR-Repeat, Rows

Decode_07
Decode_07(Source, Dest, XorFlags, XorBits);



--------------------------------------------
Decode_08or09( )
--------------------------------------------
//  Bulk Skips and Bulk Repeats, Columns

Decode_08
Decode_08(Source, Dest, Skipped);

--------------------------------------------
//  Bulk Skips and Bulk Repeats, Rows

Decode_09
Decode_09(Source, Dest, Skipped);



--------------------------------------------
Decode_0Aor0B( )
--------------------------------------------
//  Write Data Bytes or Multiple Skips, Columns

Decode_0A
Decode_0A(Source, Dest, Skipped);

--------------------------------------------
//  Write Data Bytes or Multiple Skips, Rows

Decode_0B
Decode_0B(Source, Dest, Skipped);

--------------------------------------------

default	:
	TmpStr.Format("Unknown Image Type 0x%02x",ch);
	DebugShiftKeyMsgStrPrint(TmpStr);
	return PLANE_STATUS_UNKNOWN_TYPE;

--------------------------------------------
```

```
ReadNext8BitValue
ReadNextBit
WriteNext8BitValue

GetROMAddressFromWPCAddrAndPage
ExtractWPCAddrAndPageFromBuffer
GetROMAddressFromAddrOf3ByteWPCAddrPage

PreAnalyzeVariableSizedImageTable
ExtractWPCAddrAndPageOfImageTable
GetROMAddressOfVariableSizeImageIndex
GetROMAddressOfVariableSizeImageTable
GetAddrToWPCAddressOfVariableSizeImageTable
GetVariableSizedImageTableMetadata

GetPrevImageIndex
GetNextImageIndex
GetFirstImageIndex
GetLastImageIndex

IncrementVariableSizedImageIndex
DecrementVariableSizedImageIndex

DecodeVariableSizedImageData
DecodeVariableSizedImageDataIndexToPlane


DMD_ROWS
DMD_COLUMNS
DMD_PAGE_BYTES

PAGE_LENGTH
BASE_CODE_ADDR_PAGED_ROM
BASE_CODE_ADDR_NONPAGED_ROM
NONPAGED_LENGTH
NONPAGED_BANK_INDICATOR

IMAGE_CODE_MONOCHROME
IMAGE_CODE_FD
IMAGE_CODE_BICOLOR_INDIRECT
IMAGE_CODE_BICOLOR_DIRECT

PLANE0_ON
PLANE0_XORED
PLANE0_SKIPPED
PLANE1_ON
PLANE1_XORED
PLANE1_SKIPPED


PLANE_STATUS_VALID
PLANE_STATUS_INVALID
PLANE_STATUS_UNKNOWN_TYPE
PLANE_STATUS_UNIMPLMENTED_TYPE
PLANE_STATUS_TABLEENTRYOUTOFRANGE
PLANE_STATUS_BADDIMENSION
PLANE_STATUS_IMAGEOUTOFRANGE

COMMONData 
{
	ROMSize
	TotalPages
	BasePageIndex
}

DMDPlane[DMD_PAGE_BYTES]
```
