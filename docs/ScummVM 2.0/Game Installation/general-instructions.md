---
layout: default
title: General Instructions
parent: Installing Games
nav_order: 1
---

## General Instructions

For most games simply copy the files listed on the game datafiles page for your game from the floppy or CD to your hard drive.

For some games the files are packed and not directly accessible on the floppy or CD. In such a case you will need to run the original game installer and then copy the files from where they have been installed to the directory in which you want to install the game to play with ScummVM. For DOS games you can try to use DosBox to run the installer. For Windows games if you don't have Windows you can try Wine (or Darwine on Mac OS X).

Also some games (e.g. multi-CD games) need a bit more work to be installed. See the General Notes and Games Specific instructions below.

Once the game files are on the hard drive, start ScummVM, click on Add Game (see also Adding a game) and then you are ready to play.

---
## General Notes

### Case sensitivity

Most instructions are written for the PC versions (which in some case is the only version) of the games. Windows and DOS use case-insensitive ﬁle systems, so if one CD has a ﬁle called MONKEY.DAT and another has a ﬁle called monkey.dat, they are the same ﬁles. These instructions give ﬁle names in all lower-case names, even if that’s not always how they appear on the CDs. In fact, on case-sensitive ﬁle systems you will have to make sure that all ﬁlenames use either all upper- or all lower-case letters for ScummVM to be able to ﬁnd the ﬁles.

### Multi-CD Games

In general, ScummVM does not deal very well with multi-CD games. This is because ScummVM assumes everything about a game can be found in one directory. Even if ScummVM does make some provisions for asking the user to change CD, the original games usually install a small number of ﬁles to hard disk. Unless these ﬁles can be found on all the CDs, ScummVM will be in trouble.

Fortunately, ScummVM has no problems running the games entirely from hard disk, if you create a directory with the correct combination of ﬁles. Usually, when a ﬁle appears on more than one CD you can pick either of them.

### Macintosh games: Accessing HFS Filesystems

You will need the "Windows Installer" from the download page. To copy the game data file from the CD to your hard disc, you will need HFVExplorer. Make sure you get the "HFV Explorer installer" rather than the zip file. When you choose to download the zip file, make sure you read the readme included with HFVExplorer, to set it up properly. Run the HFVExplorer installer and allow it to use its defaults. Alternatively you can also use the more recent HFSExplorer.

Start up HFVExplorer; if you don't have a shortcut for it, find it in "C:\Program Files\HFVExplorer". It should open the HFS (Macintosh filesystem) CD-ROM automatically when you insert the disc. Make sure HFVExplorer is displaying hidden files: Select View->Options and enable "Show invisible Mac files" on the "File attributes" tab.

Now, look for the data file in the right pane. It will probably end with the word "Data" and will be the largest file on the volume. For instance (using Sam & Max Hit the Road as an example), it is called "Sam & Max Data" on the "Sam & Max" CD-ROM. Select the data file and copy it (use Ctrl+C or Edit->Copy). In the left HFVExplorer pane, navigate to the directory where you want the game to reside on your hard disc. We recommend selecting drive C: and creating a new folder called "SamNMax" or a name that better reflects your particular game.

Paste the data file (with Ctrl+V or Edit->Paste) and allow HFVExplorer to choose the copy mode. Now, wait while the program copies several hundred megabytes from the CD. When the file is copied, close HFVExplorer.

### Datafiles

For a comprehensive list of required Datafiles for supported games visit: [Here](https://wiki.scummvm.org/index.php/Datafiles).

### Extra Datafiles

Some games require additional files that are not part of the original data. Those files can generally be found in our Downloads page.

Games that require additional data:

- Beneath a Steel Sky (sky.cpt)
- Flight of the Amazon Queen
- Kyrandia Series (kyra.dat)
- Lands of Lore Series (kyra.dat)
- Lure of the Temptress (lure.dat)
- Versailles 1685 (cryomni3d.dat)

The most up to date list of Engine data files can be found in our [source code repository](https://github.com/scummvm/scummvm/tree/master/dists/engine-data)