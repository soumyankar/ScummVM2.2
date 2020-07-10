---
layout: default
has_children: false
parent: Guides
title: Using the CLI
nav_order: 7
---

# Using the CLI

You can access all tools through the command line interface using the following syntax:

``` ./scummvm-tools-cli [audio mode params] [params] [-o output] [extract|compress] <inputfile N ...> ```

Normally, all arguments except the input file(s) can be skipped. You can specify extract or compress before the filename to hint the tool what activity you want to perform. In many cases, the tools will output to the directory "out/" relative to the input file, if no directory is specified.

Some tools take additional parameters, use ```--help <tool name>``` to display extra arguments for that tool.

Use ```--list``` to display a list of all supported tools.

Use the -o or --output flag to specify the output file, if it's a directory, it's strongly recommended to append / to the filename for clarity. Normally the tools will output to the directory "out/" relative to the input file, if no directory is specified, some tools output to a file instead of a directory.

You can also specify the tool explicitly to ignore automatic detection:

```./scummvm-tools-cli --tool <tool name> [audio mode params] [params] [-o output] <inputfile N ...>```


## Audio mode params

You can specify what compression method to use. Use ```--mp3```, ```--flac``` or ```--vorbis``` first to select a special format, default is MP3.

### MP3 mode params (version 1.1.1)

- -b rate — rate is the target bitrate(ABR)/minimal bitrate(VBR).
- -B rate — rate is the maximum ABR/VBR bitrate.
- --vbr — LAME Uses the VBR mode (default).
- --abr — LAME Uses the ABR mode.
- -V value — Specifies the value (0 - 9) of VBR quality (0 being the best quality).
- -q value — Specifies the MPEG algorithm quality (0 - 9) (0 being the best quality).
- --silent — The output of LAME is hidden.
- --lame-path — Specifies the path to lame (default: lame).

### MP3 mode params (version 1.2.0svn)

- --vbr — LAME Uses the VBR mode (default).
- --abr rate — LAME Uses the ABR mode with the given target bit rate.
- --cbr rate — LAME Uses the CBR mode with the given bit rate.
- -b rate — rate is the minimum ABR/VBR bitrate (undefined by default).
- -B rate — rate is the maximum ABR/VBR bitrate (undefined by default).
- -V value — Specifies the value (0 - 9) of VBR quality (0 being the best quality).
- -q value — Specifies the MPEG algorithm quality (0 - 9) (0 being the best quality).
- --silent — The output of LAME is hidden.
- --lame-path — Specifies the path to lame (default: lame).

### Vorbis mode params

- -b rate — rate is the nominal bitrate.
- -m rate — rate is the minimum bitrate.
- -M rate — rate is the maximum bitrate.
- -q value — Specifies the value (-1 - 10) of VBR quality 10 is best quality.
- --silent — The output of oggenc is hidden.

### Flac mode params

- --fast — FLAC uses compression level 0.
- --best — FLAC uses compression level 8.
- -value — Specifies the value (0 - 8) of compression, with 8 being the best quality.
- -b value — Specifies a blocksize of value samples, must be a multiple of 8 between 8 and 160.
- --verify' — Files are encoded and then decoded to check accuracy.
- --silent — The output of FLAC is hidden