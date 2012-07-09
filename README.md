# lzmaSDK

7zip is a useful replacement for zlib and bzip2. In some cases, 7zip can achive drastically better compression ratios than both zlib and bzip2. One can always go to [7-zip.org](http://www.7-zip.org/) to find the source code. This example provides the lzma SDK (release 9.21 beta) configured as an iPhone project.

This repository is a clone of Mo DeJong's work and is here to be integrated in CocoaPods Spec repo. You can find the original packed zip file here: [Example 7](http://www.modejong.com/iOS/).

This repository contains the LZMA SDK customized for an embedded system (iPhone/iOS). Only the file extraction logic was included, all code related to creating compressed streams was removed. Also, CRC validation was removed to improve performance. This is based on **lzma release 9.21 beta**.

Embedded version does not need exe branch predictors:

* Bra.c
* Bcj2.c
* Bra86.c

## File List:

* 7zBuf.c
* 7zBuf.h
* 7zCrc.c
* 7zCrc.h
* 7zFile.c
* 7zFile.h
* Archive
* CpuArch.h
* LzHash.h
* LzmaDec.h
* LzmaDec.c
* Types.h

## Removed:

* Xz.* (XZ file format support)
* MtCoder.c
* Ppmd7Enc.c
* Sha256.*
* lzma Serch (encode) functions
* rm LzFind*
* rm Threads.*
* rm Bra*
* rm Bcj2.*
* rm lzmaEnc* lzma2Enc.*

To update to a new version of the LZMA SDK, use the update.tcl to copy over those
files that were used in this version.