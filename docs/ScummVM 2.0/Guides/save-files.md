---
layout: default
has_children: false
parent: Guides
title: Save Files
nav_order: 1
---

# Save Files

Save Files are by default put in the current directory on some platforms and oreset directories on others. You can specift the save ub the config file by setting the savepath parameter.

Platforms that currently have a differnet default directory are:
- Mac OS X
- Windows Vista
- ..and others.

## Autosaves
For some games ScummVM will by default automatically save the current state every five minutes (adjustable via the autosave_period config setting). The default autosave slot for many engines is slot 0.

The games/engines listed below have autosave support.

- AGI games
- Beneath a Steel Sky
- Bud Tucker in Double Trouble
- COMPOSER games
- Flight of the Amazon Queen
- Myst
- Riven
- SCUMM games
- The Legend of Kyrandia I (slot 999)
- ZVISION games

For the SCUMM engine, this saved game can then be loaded again via Ctrl-0, or the F5 menu.

## Converting Saved Games

Using saved games from original versions isn't supported by all game engines. Only the following games can use saved games from their original versions.

### Blade Runner

- Use the debugger console and command "save" to save the game to the original format and command "load" to load such a one
- Saved games between different languages are interchangeable
- It is not recommended to convert saved games from the version with restored content as they might behave unexpectedly or might cause game breaking bugs

### Elvira 1

- Add 8 bytes (saved game name) to the start of the saved game file
- Rename the saved game to ```elvira1.xxx```

### Myst

- Rename the saved game to myst-xxx.mys
- Saves from the masterpiece edition and the regular edition are interchangeable

### Starship Titanic

- Rename the saved game to titanic-win.xxx for saves from the English version and titanic-win-de.xxx for saves from the German version
- Saved games between different languages are not interchangeable

_and lots others_

## Viewing/Loading saved games from the command line

```--list-saves```

This switch may be used to display a list of the current saved games of the specified target game and their corresponding save slots. If no target is specified, it lists saved games for all known target.

Usage: ```--list-saves --game=[TARGET]```, where ```[TARGET]``` is the target game.

Engines which currently support ```--list-saves``` are:

- AGI
- AGOS
- BLADERUNNER
- CGE
- CINE
- CRUISE
- CRYOMNI3D
- DRACI
- GROOVIE
- HUGO
- KYRA
- LURE
- MOHAWK
- PARALLACTION
- QUEEN
- SAGA
- SCI
- SCUMM
- SKY
- SWORD1
- SWORD2
- TEENAGENT
- TINSEL
- TITANIC
- TOON
- TOUCHE
- TSAGE
- TUCKER
- ZVISION

```--save-slot/-x```

This switch may be used to load a saved game directly from the command line.

Usage: ```--save-slot[SLOT]``` or ```-x[SLOT]```, where ```[SLOT]``` is the save slot number.

Engines which currently support ```--save-slot / -x``` are:

- AGI
- AGOS
- BLADERUNNER
- CGE
- CINE
- CRUISE
- CRYOMNI3D
- DRACI
- GROOVIE
- HUGO
- KYRA
- LURE
- MOHAWK
- PARALLACTION
- QUEEN
- SAGA
- SCI
- SCUMM
- SKY
- SWORD1
- SWORD2
- TEENAGENT
- TINSEL
- TITANIC
- TOON
- TOUCHE
- TSAGE
- TUCKER
- ZVISION
