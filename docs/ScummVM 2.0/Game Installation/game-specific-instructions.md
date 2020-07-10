---
layout: default
title: Game-Specific
parent: Installing Games
nav_order: 2
---

# Game-Specific Instructions

## LucasArts Games (SCUMM Engine)

### The Curse of Monkey Island

For this game, you will need the comi.la0, comi.la1 and comi.la2 files. The comi.la0 file can be found on either CD, but since they are identical it doesn't matter which one of them you use.

In addition, you will need a resource subdirectory with all of the files from the resource subdirectories on both CDs. Some of the files appear on both CDs, but again they're identical.

### Macintosh Games

All LucasArts SCUMM based adventures except Curse of Monkey Island also exist in versions for the Macintosh. ScummVM can use most (all?) of them, however, in some cases some additional work is required.

First off, if you are not using a Macintosh for this, accessing the CD/floppy data might be tricky. See notes in the Accessing HFS filesystems section.

Most of the newer games on the Macintosh shipped with only a single data file (note that in some cases this data file was made invisible, so you may need extra tools in order to copy it). ScummVM is able to directly use such a data file; simply point ScummVM at the directory containing it, and it should work (just like with every other supported game).

We also provide a tool called ```'extract_scumm_mac'``` in the tools package to extract the data from these data files, but this is neither required nor recommended.

### Maniac Mansion NES

Supported versions are English GB (E), French (F), German (G), Swedish(SW) and English US (U). ScummVM requires just the PRG section to run and not the whole ROM.

In order to get the game working, you will have to strip out the first 16 bytes from the ROM you are trying to work with. Any hex editor will work as long as you are able to copy/paste. After you open the ROM with the hex editor, copy everything from the second row (17th byte) to the end. After you do this, paste it to a new hex file. Name the new file "Maniac Mansion (XX).prg" while XX stands for the version you are working with (E, F, G, SW, or U). The final size should be exactly 262144 bytes.

If you add the game manually make sure that the platform is set to NES.

Most common mistakes which prevents the game from running:

- Bad file
- ROM extracted with the 0.7.0 tools
- You try to feed ScummVM with the FULL ROM and not just the PRG section.

It is also possible to extract the separate LFL files from the PRG section. To do so use the ```'extract_mm_nes' utility``` from the tools package.

### Maniac Mansion Commodore 64

This games is detected and runs in ScummVM but is not yet completable. Simply name the D64 disks "maniac1.d64" and "maniac2.d64", then ScummVM should be able to automatically detect the game if you point it at the right directory.

Alternatively, you can use ```'extract_mm_c64'``` from the tools package to extract the data files. But then the game will not be properly auto-detected by ScummVM, and you must make sure that the platform is set to Commodore64. We recommend using the much simpler approach described in the previous paragraph.

### Zak McKracken Commodore 64

Rename the D64 disks "zak1.d64" and "zak2.d64", then ScummVM should be able to automatically detect the game if you point it at the right directory.

Alternatively, you can use 'extract_zak_c64' from the tools package to extract the data files. But then the game will not be properly auto-detected by ScummVM, and you must make sure that the platform is set to Commodore64. We recommend using the much simpler approach described in the previous paragraph.

## Revolution Software Games

### Beneath a Steel Sky

In August 2003, the creators and copyright holders of Beneath a Steel Sky, Revolution Software, released the game as freeware for use with ScummVM. You can therefore download the game from our Downloads page. Then follow the general instructions.

Starting with ScummVM 0.8.0 you need the additional 'SKY.CPT' file to run Beneath a Steel Sky. This file is distributed with ScummVM on most platforms. You can place it in either the directory containing the other game data files (SKY.DNR, SKY.DSK), in your extrapath, or in the directory where your ScummVM executable resides.

### Broken Sword 1

For this game, you will need all of the ﬁles from the clusters directories on both CDs. You will also need the speech.clu ﬁles from the speech directories, but since they are not identical you will need to rename them speech1.clu and speech2.clu for CD 1 and 2 respectively.

In addition, you will need a music subdirectory with all of the ﬁles from the music subdirectories on both CDs. Some of these ﬁles appear on both CDs, but in these cases they are either identical or, in one case, so nearly identical that it makes little difference.

Starting with ScummVM 1.0.0, the original Smacker cutscenes (.smk files) are supported without having to download a video pack from the website. To use them you will need to copy the files from the smackshi directories of both CDs. You can ignore the smackslo directories since they contains lower quality versions of the same cutscenes.

### Broken Sword 2

For this game, you will need all of the ﬁles from the clusters directories on both CDs. (Actually, a few of them may not be strictly necessary, but the ones that I’m uncertain about are all fairly small.) You will need to rename the speech.clu and music.clu ﬁles speech1.clu, speech2.clu, music1.clu and music2.clu so that ScummVM can tell which ones are from CD 1 and which ones are from CD 2. Any other ﬁles that appear in both cluster directories are identical. Use whichever you like.

In addition, you will need the cd.bin, cd.inf and startup.inf ﬁles from the sword2 directory on CD 1.

Starting with ScummVM 1.0.0, the original Smacker cutscenes (.smk files) are supported without having to download a video pack from the website.

## Adventure Soft Games

### Simon the Sorcerer 1 and 2

If you have the dual version of Simon the Sorcerer 1 or 2 on CD, you will find the Windows version in the main directory of the CD and the DOS version in the DOS directory of the CD. Both are supported by ScummVM but depending on the version you want to use you will not need to copy the same files (see the game datafiles page for more details).

### The Feeble Files

The following instructions are valid for the Windows versions of the game. Depending on the version that you have, you will have either two CDs or four CDs. The instructions to use this game with ScummVM are nearly the same for both versions.

You will need to copy all the files listed in the game datafiles page in a directory on your hard drive. Some of the files can be copied directly from the CDs and others are packed into an InstallShield Cabinet file (the files with the .cab extension). For the later you will either need to run the installer on Windows (or using Wine or Darwine on Linux and Mac OS X respectively) or to unpack the files using the i5comp decompression tool (unshield has been reported to fail on these files). After running the installer you can copy the files from where they were installed to the directory in which you are copying all the files for ScummVM.

During the copy you have to pay special attention to the voices.wav files. There is one on each CD and they are different. Therefore you will have to rename them so that you can copy all of these files in the same directory. Rename voices.wav from CD1 to voices1.wav and voices.wav from CD2 to voices2.wav. If you have the four CDs version you will also need to rename voices.wav from CD 3 and 4 to voices3.wav and voices4.wav respectively.

Starting from version 0.13.0 ScummVM can read the original Smacker video files (the files with the .smk extension). If you are using an older version of ScummVM you will need to re-encode the video files using the RAD Video Tools and the ```'encode_dxa' tool``` (or ```'convert_dxa.bat'``` batch file).

## Other Games

### Flight of the Amazon Queen

In March 2004, the creators and copyright holders of Flight of the Amazon Queen, John Passfield and Steve Stamatiadis, released the game as freeware for use with ScummVM. You can therefore download the game from our Downloads page. Then follow the general instructions.

If you have the original CD of the game game and would like to play this version, you will also need the 'queen.tbl' file. This file is distributed with ScummVM on most platforms. You can place it in either the directory containing the 'queen.1' file, in your extrapath, or in the directory where your ScummVM executable resides.

Alternatively you can use the ```'compress_queen'``` tool from the tools package to 'rebuild' your FOTAQ data file to include the table for that specific version, and thus removing the run-time dependency on the 'queen.tbl' file. This tool also allows you to compress the speech and sound effects with MP3, OGG or FLAC.

### The Legend of Kyrandia

To run The Legend of Kyrandia under ScummVM you need the 'kyra.dat' file. This file is distributed with ScummVM on most platforms. You can place it in either the directory containing the other game data files, in your extrapath, or in the directory where your ScummVM executable resides.

### Drascula: The Vampire Strikes Back

In August 2008, the creators and copyright holders of Drascula: The Vampire Strikes Back, Alcachofa Soft, released the game as freeware for use with ScummVM. It is available for download from our Downloads page.

1. You will need to download the English version (even if you want to play it in another language). You will also need the 'DRASCULA.DAT' file. This file is distributed with ScummVM on most platforms. You can place it in either the directory containing the 'PACKET.001' game data file, in your extrapath, or in the directory where your ScummVM executable resides.
2. Then if you want to play the game in another language (Spanish, German, French or Italian) you will also need to download the international pack and put the files together with the English version file (i.e. have all the PACKET.00# and DRASCULA.DAT files in the same directory).
3. Finally to play the game with a music score you will need to download the Music Add-on and put the ogg files together with the other game files.
4. Then follow the general instructions to add the game in ScummVM. If you have installed the international pack, it will ask you in which language you want to play the game when adding it in ScummVM. You can add the game several times with a different language if you want to. The English and Spanish versions both have voice over in that language. The other versions will use English voice over with subtitles in the language you selected.  

Note: in the Music add-on the ogg files are in an audio directory, if you keep them in that directory you will need to add it in the Game extra path. To do so, after adding the game in ScummVM, select the game in the ScummVM launcher and click on Edit Game. Then go to the Paths tab and in Extra Path add the path to the Music directory in which all the ogg files should be. Alternatively you can move all the ogg files in the same directory where you have the data files (the PACKET.00# files), and it will pick up the music without having to select an extra path.

### Fascination

In order to get the game working, you will have to extract the STK files hidden on the CD. In order to do so, create an ISO of the first (data) track on your original disc (~11M, not 652M), then use the ```'extract_fascination_cd'``` utility from the tools package to create the four STK files and copy those files to the game directory. The game also uses the following audio track containing the speech. Extract it and compress it as per other games with CD-DA audio, then copy it to the game directory (named as track1.mp3).  

### Blade Runner

You need to create a game directory and copy the required data files in there from the four CDs.  

- Note that you may copy the CDFRAMES.DAT files from the CDs into the game directory, renaming the files from the first, second, third and fourth CD to CDFRAMES1.DAT, CDFRAMES2.DAT, CDFRAMES3.DAT and CDFRAMES4.DAT respectively.
- 	_Alternatively_, you may use the 'pack_bladerunner' utility from the tools package to create a single HDFRAMES.DAT file from the partial CDFRAMES.DAT files located on the four CDs; this newly created HDFRAMES.DAT file should then be copied in the game directory.

Please make sure that, when you add your Blade Runner game directory to ScummVM, the Save Path folder is a folder for which you have write permission, so that auto-saves and manually saved games work properly.

For **subtitles support**, you may download the SUBTITLES.MIX file provided by ScummVM and put it in the game directory. Currently, the provided file will work with the all available and supported localized versions of the game but will only show English subtitles in all but the French version, which will show French subtitles.

However, other localized versions of the subtitles (and the game's user interface) may also be supported in the future. ScummVM offers a semi-automated process to pack a localized transcript from an Excel file (of appropriate structure) into a SUBTITLES.MIX file. This process, along with usage instructions for the ScummVM developer tools involved, is described in detail on a [ScummVM GitHub page](https://github.com/scummvm/scummvm/tree/master/devtools/create_bladerunner/subtitles).