## v0.29 (Jan 08, 2018)

* **Engine :**
  * k2engine: Handling the callback function call if the plugin module fails to load
  * k2engine: Processing to render the result of recompression in detail after malicious code in the compressed file is processed
  * k2engine: Fixed the problem that the extension can not be removed properly if the kmd file path name has a period (.)
  * k2engine: Fixed an infinite loop problem in case of malfunction code failure
  * k2engine: Process temporary folders by process
  * k2file: Add a class to process temporary folders by process

* **Plugins Modules :**
  * adware: new support
  * attach: process to add size information of an attached image to newly extract an attached image
  * bz: New support
  * carch: New support
  * dde: New support
  * egg: new support
  * elf: verbose processing on ELF 64bit
  * emalware: Handle MD5 calculations if section size is 0
  * emalware: Handle malicious code in addition to .text area
  * gz: New support
  * kavutil: MD5 pattern is compressed so that it is decompressed and then loaded
  * ole: Added malicious code remedy to infected ole file
  * ole: Correct the processing for bad access and the PPS length to be 0x40 max.
  * ole: Eliminate unnecessary logic
  * ole: Exploit.OLE.CVE-2003-0347 Add inspection logic
  * ole: Opening ole file in write mode to handle failure to delete stream
  * olenative: Added malicious code remediation to Ole10Native files
  * pdf: Add malware PDF signature test signature
  * pdf: Added Trojan.PDF.Generic inspection logic
  * pdf: Improved inspection speed by avoiding unnecessary stream extraction
  * pe: Do not calculate MD5 if section size is 0
  * pe: Error handling to divide by 0 in converting RAV to Offset
  * pe: If there is a digital signature, the position and size of the attached image are newly processed
  * pe: Processing parsing failure if there is not enough data in the .rsrc area
  * pyz: Added pyc type malicious code
  * pyz: Improved error by checking TOC type
  * pyz: New support
  * tar: New support
  * unpack: Exceptions when zlib is not a compressed object
  * unpack: Process zlib and embed_ole simultaneously to recognize format
  * unpack: add infected malicious code remedy to embed ole file
  * upx: Add exception handling for uncompressed sizes
  * upx: Fixed an issue where execution compression was not released
  * xz: New support
  * yaraex: Engine initialization failure processing when there is no yara module

* **Command Line Interface :**
  * k2: engine initialization failure processing when there is no yara module
  * k2: Processing to prevent the same malicious code inspection result from being output
  * k2: Easily recognizable by adding a comma (,) to the number of malicious code patterns loaded
  * k2: Outputs error message after processing residual printout when nonexistent Paht check
  * k2: Output the plug-in module that failed to load as an error message
  * k2: Processing to render the result of recompression in detail after malicious code in the compressed file is processed
  * k2: Processing to prevent redundant output when expressing the result of re-compression in detail
  * k2: Change the update file to a gz file and process the update itself
  * k2: Change update path
  ** Related Issue: https://github.com/hanul93/kicomav/issues/4
  * k2: Fixed error when scrolling while printing Windows 10 legacy console
  ** Related Issue: https://github.com/hanul93/kicomav/issues/7

* **Tools :**
  * sigtool_md5: Reduce capacity by compressing MD5 pattern
  * sigtool_md5: Prevent duplicate malware name generation
  * sigtool_yar: New support

## v0.28 (Sep 04, 2017)

* **Engine :**
  * Improved decompression speed of compressed files
  * Added resource parsing function for PE file
  * Added malware scanning function using YARA rule
  * Fixed product hang when extracting ZIP files with errors
  * Fixed errors when scanning ZIP and HWP files with passwords

## v0.27b (May 22, 2017)
* **Engine :**
  * Fixed for pylzma import error

## v0.27a (May 17, 2017)
* **Interface :**
  * Enabled update option (--update)

## v0.27 (May 4, 2017)
* **Engine :**
  * Redesigned an architecture of KicomAV

## v0.26 (June 16, 2016)
* **File Formats :**
  * BinData/BIN0001.OLE in HWP File
* **Engine :**
  * APK(Android) Engine
  * OleNative Engine
  * Embeded Engine
  * Base1 Engine

## v0.25 (July 18, 2013)
* **File Formats :**
  * UPX
  * Attached File
* **Engine :**
  * COFF Engine

## v0.24 (July 7, 2013)
* **File Formats :**
  * ALZ
  * EGG
* **Engine :**
  * Macro Virus for MSWord & MSExcel

## v0.23 (June 27, 2013)
* **File Formats :**
  * PE
* **Engine :**
  * MD5 Scan for PE 
* **Tool :**
  * Display **Signature number & Last update** Information
  * Support Multi scan paths
  * Signature Tool (**sigtool**) ver 0.1
* **BugFix :**
  * OLE PPS Dump
  
## v0.22 (June 16, 2013)
* **File Formats :**
  * OLE
* **Engine :**
  * Hangul Word Processor(HWP) Exploit
* **Option :**
  * -V, --vlist : display virus list
  * --update : update
  * --no-color : not print color

## v0.21 (June 11, 2013)
- Add Command line Option : -r (scan archives)
- Support for ZIP

## v0.20b (June 1, 2013)
- Command line support : k2.py

## v0.20a (May 28, 2013)
- Add build.sh

## v0.20 (May 27, 2013)
- Redesigned **Plug-in** architecture

## v0.1a (May 15, 2013)
- Automated unit-testing for KicomAV using **Travis-CI**

## v0.1 (May 8, 2013)
- **Initial release**