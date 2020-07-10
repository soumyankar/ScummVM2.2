---
layout: default
title: Port-Specific
parent: Installing Games
nav_order: 3
---

# Port Specific Instructions

The following section talk about installing games on various platforms.

## Dreamcast
TODO

## GameCube
TODO

## GP2X / GP2XWiz
TODO

## iPhone / iPod Touch

To copy the game data files over to your device:

- On the iPhone/iPod install OpenSSH (if it is not already installed), using Cydia.
- Install an SFTP client (For Macs, Cyberduck is good. For Windows, FileZilla should do the trick). Then connect your SFTP client to your iPhone/iPod using the IP address the device shows in its network settings (Hit Settings, then Wi-Fi, then find the network you're connected to). The username is "root" and the password probably "alpine".
- Make a subdirectory on your phone under /var/mobile (or /var/root for firmware versions 1.1.2 and below), and upload the games there (don't place them anywhere else on the phone, as you'll be filling up the smaller system partition then). Here you can see exactly which files you need for which games.
- Make sure these files and directories have the right permissions set! You're uploading as root, all the files need to be readable by the 'mobile' user as well.
- When you've uploaded all the games you want, start up ScummVM and add the game(s) there (navigate to the same directory you uploaded them to).

## Maemo

Connect the device via USB and copy the games files to the device following guidelines from the General Instructions section.

## Nintendo DS

Copy the games you want to play onto the MicroSD card on which you have installed ScummVM (see Installing ScummVM). The game files can be copied in any location, one game per folder. Then you just have to boot the DS with the MicroSD card and card reader inserted and run ScummVM.

To decrease the memory usage ScummVM for Nintendo DS has been split into several builds. Depending on the game you want to play you will have to run the correct build. Even so, some of the games cannot be run on a Nintendo DS because they require too much memory. You can find the list of supported games and which build you need to use for each one in the readme_ds.txt file present in the ScummVM Nintendo DS package. This information is also available on the Nintendo DS page.

## Playstation 2

TODO

## PSP
TODO

## Symbian
TODO

## Wii
TODO

## Windows CE

You can find installation instructions for devices running Windows CE on the Windows CE page.
