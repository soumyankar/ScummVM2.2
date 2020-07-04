---
layout: default
parent: Troubleshooting
nav_order: 2
title: Mac Games
---

# Mac Games

This is a HOWTO for extracting data from Macintosh games.

## Getting the data

### Windows

#### HFVExplorer

In order to be able to read Mac floppies and CD's, you will need to download HFVExplorer. Make sure you get the "HFV Explorer installer" rather than the zip file. If you choose to download the zip file, make sure you read the readme included with HFVExplorer, to set it up properly.

After inserting your media, start up the program. Make sure HFVExplorer is displaying hidden files: Select View->Options and enable "Show invisible Mac files" on the "File attributes" tab.

Select the files and folders you want to extract. Then copy it by pressing ctrl+c or going to edit->copy. Navigate to where you want to copy the data. Then paste by pressing ctrl+v or going to edit->paste.

A "Select copy mode" window will pop up. If you need a resource fork, you want to extract it as "MacBinary 2". Otherwise, you want to extract it as "Raw copy, data fork". If you don't know what you need, please see the Datafiles page to see if it says "resource fork" under the name

#### HFSExplorer

Alternatively, you can use HFSExplorer to extract data.

### Linux

#### Ubuntu

Working as of 9.04 (Jaunty).

##### Command line

- Install hfsutils (e.g. sudo aptitude install hfsutils)
- If you don't already know it, find the device name of the drive the disc is in (e.g. doing eject /dev/cdrom type commands is a good way)
- Run hmount /dev/devicename. This will let all the other hfsutils know what they should refer to
- Use hls, hcd, hcopy to copy all the required files to your hard disc (man hfsutils will list all the available commands)
	- Use the -m hcopy option to use the MacBinary format if you need the resource fork
	- Use the -r hcopy option to copy only the Raw data if you don't need the resource fork
- You can optionally use macutils to manage mac files after you've copied them (with this you can extract concrete forks, convert between formats, repackage several forks into a MacBinary, etc.)

### Mac OS X

Fortunately, Mac OS X already supports HFS discs. When you copy the data off the discs it should be able to copy it with both resource and data fork already, which ScummVM can handle out of the box.

If there are hidden files, you can use this Terminal command for showing hidden files in the Finder

```defaults write com.Apple.Finder AppleShowAllFiles true```

followed by relaunching the Finder (cmd+opt+esc, and then select Finder). To turn off hidden files again, repeat the command but change true to false.

### Naming Resource Forks

This section mostly pertains to people not using Mac OS X.

If you have a file with a resource fork, you have to name the file in a certain way for ScummVM to pick up on it. If you have a MacBinary file, please make sure it has a ".bin" extension. If you have a raw resource fork, please make sure it has a ".rsrc" extension.