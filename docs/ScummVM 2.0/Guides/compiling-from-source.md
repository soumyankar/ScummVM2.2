---
layout: default
has_children: false
parent: Guides
title: Compiling from Source
nav_order: 4
---

# Compiling from Source
ScummVM is written in C++ and has been ported to several different platforms. Compilation of ScummVM is different for each platform, please take care with the instructions.

If you are compiling for Windows, Linux or Mac OS X, you need SDL-1.2.2 or newer (older versions may work, but are unsupported), and a supported compiler. Several compilers, including GCC, mingw and recent versions of Microsoft Visual C++ are supported. If you wish to use MP3-compressed CD tracks or .SOU files, you will need to install the MAD library; likewise you will need the appropriate libraries for Ogg Vorbis and FLAC compressed sound. For compressed save states, zlib is required.  

Some parts of ScummVM, particularly scalers, have highly optimized versions written in assembler. If you wish to use this option, you will need to install [nasm assembler](https://www.nasm.us/). Note that we currently only have x86 MMX optimized versions, and they will not compile on other processors.  

On Windows, you can define USE_WINDBG and attach ```WinDbg``` to browse debug messages see [here](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/index).

- Windows
	- MinGW
		- Please [refer](https://wiki.scummvm.org/index.php/Compiling_ScummVM/MinGW).
	- Visual Studio (MSVC)
		- Please [refer](https://wiki.scummvm.org/index.php/Compiling_ScummVM/Visual_Studio).

Discontinued; Need advice.
