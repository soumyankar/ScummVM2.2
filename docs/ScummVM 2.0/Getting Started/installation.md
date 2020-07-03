---
layout: default
title: Installation
parent: Quick Start
nav_order: 2
---

# Installation

After you have obtained ScummVM as described in the previous section, you will probably want to install it on your system. The steps required for that differ between the various operating systems. ScummVM recommends most users to download the pre-built binaries. Refer below for the OS you want to run ScummVM on.

### Amiga OS4

```
- Download the AmigaOS4 package from the downloads page. You will download a packed archive (.lha).
- To unpack the archive, double click on it, and UnArc will either unpack right away or ask for the installation path.
- Once it is unpacked, you can move the whole drawer wherever you wish to store it.
```
### Atari
TODO

### BeOS
TODO

### Debian
If you have the latest stable version of Debian then:  
```
- From the [httpss://www.scummvm.org/downloads/ downloads page], download the Debian (.deb) package.
- To install it, you need to be root and type dpkg -i packagename.deb into a virtual terminal near you.
```

If you are running Debian testing or unstable then:  
```
- The latest version of ScummVM should already be available in the repositories
- To install it, type apt-get install scummvm into a virtual terminal near you.
- If it still is not the latest version, then go bug the Debian package maintainer (see [[Developers Bios]) about it.
```

To launch the GUI application, simply type scummvm in your terminal.

### Dreamcast

```
- From the downloads page, download either the Dreamcast .tar.bz2 file or the Nero image file.
```

If you download the .tar.bz2 file:  
```
- Use any archiver program (for eg. WinZip) to open it.
- After opening the archive, copy it to the folder where you want to put it.
```

If you download the Nero image file:  
```
- It can be burned automatically to a CD using Nero Burning ROM or any other program that accepts NRG formatted disc images.
```

### Fedora Core / Red Hat
TODO

### GP2X / GP2XWiz
TODO

### iPhone

**Cydia (Firmware 2.0 and upwards)**
- Start Cydia
- On the main Cydia tab (the Home screen), click "More Package Sources"
- Select and install the UrbanFanatics.com source
- ScummVM should now be in "Games" section, ready for you to install!

**Installer.app (Firmware 1.1.4 and below)**  
- Open Installer.app on a jailbroken iPhone or iPod touch. Use Google to find out how to jailbreak your specific version of the firmware on your device.
- Tap the "Sources" button in the bottom-right corner.
- Tap the "Edit" button in the top-right corner.
- Tap the "Add" button in the top-left corner.
- Enter http://urbanfanatics.com/scummvm.xml into the text area and tap "OK".
- Installer will refresh your sources. It may close. If so, reopen it.
- ScummVM is now available for install in the Games section.

### macOS

```
- From the downloads page, download the macOS 10.7+ 64 bits package file, unless you want to use it on an older PPC or 32 bit Mac OS X system (separate packages are available for those on the download page). You will download a disk image (.dmg).
- To open it, double click on it. This will mount the image as a new Device (similar to when you plug an USB key).
- Once it is mounted, copy the files inside to a folder where you wish to store it.
```
ScummVM now also includes an auto-update options. This is not enabled by default, but you can enable it, or manually check for updates, in the ScummVM Options dialog. When a new version is available you will have the option to install it or continue with your current version.

### Maemo

```
- From the downloads page, download the Maemo package. This is a *.deb file. Save it to the tablet.
- From the Application Manager, choose the "Application"->"Install From File" menu option and select the *.deb you downloaded.
```

### Nintendo DS

To run ScummVM on your DS you will need an unofficial card reader. Once you have one working:  
```
- Download the ScummVM package for Nintendo DS from the [httsp://www.scummvm.org/downloads/#stable download page]. You will download a (.zip) file
- Unzip the file using any archiver program (for eg. WinZip).
- Copy the files on your MicroSD card using your PC card reader.
```  
To decrease the memory usage ScummVM for Nintendo DS has been split into several builds. Depending on the game you want to play you will have to select the correct build. Even so, some of the games cannot be run on a Nintendo DS because they require too much memory. You can find the list of supported games and which build you need to use for each one in the readme_ds.txt file present in the ScummVM Nintendo DS package. This information is also available on the [Nintendo DS](https://wiki.scummvm.org/index.php?title=Nintendo_DS) page.

You can find more information on how to get ScummVM to work on a Nintendo DS on [this page](http://scummvm.drunkencoders.com) which is the official website for the ScummVM Nintendo DS port.

### Nintendo GameCube
TODO

### Palm OS

```
- From the downloads page, download either the PalmOS 5 binary or the PalmOS Tapwave Zodiac binary
- Unzip the files to your computer.
- Using your HotSync tool, install the scummvm-frontend.prc and skin.pdb files to your device.
- Launch ScummVM to create the /PALM/Programs/ScummVM/ folders and subfolders on your memory card.
- Using a card reader, copy the engines you require to play your games to the /ScummVM/Mods/ folder on your card (scumm.engine for scumm games, queen.engine for FOTAQ, etc.).
```
### PlayStation 2
TODO

### PlayStation Portable

```
- Copy the relevant game datafiles to your memory stick (location doesn't matter).
- Download the latest PSP development version here
- Install ScummVM like any other homebrew.
- Run ScummVM and use the launcher to add games and run them.
- Press Start to return to the launcher and play another game.
```  
For more details, see [PSP page](https://wiki.scummvm.org/index.php?title=PlayStation_Portable#Installation).

### Slackware
TODO

### Symbian
TODO

### Wii
TODO

### Windows

```
- From the [downloads page](https://www.scummvm.org/downloads/), download either the Win32 .zip file or the Win32 .exe file.
```  
If you download the .zip file:  
```
- Use any archiver program (for eg. WinZip) to open it.
- After opening the archive, copy it to the folder where you want to put it.
```  

If you download the .exe installer  
```
- Run the installer by double-clicking on the .exe file.
- Choose the location where you want to install it. The installer will also creates a shortcut in the Start Menu.
```  
ScummVM now also includes an auto-update options. This is not enabled by default, but you can enable it, or manually check for updates, in the ScummVM Options dialog. When a new version is available you will have the option to install it or continue with your current version.  

### Windows Mobile (WinCE / PocketPC / Smartphone)

```
- Create a folder on your device to put ScummVM into, e.g. "\My Device\SD-MMcard\ScummVM".
- From the download page, download the Windows CE ARM package zip file.
- Extract this file and place it all in the folder that you created on your device
(using ActiveSync or similar: note that if your chosen location is short of space, the only absolutely required file is "scummvm.exe").
- To run ScummVM just tap on "scummvm.exe" in File Explorer
- You may wish to copy a shortcut of "scummvm.exe" to your Start Menu to allow for easier access.

```
