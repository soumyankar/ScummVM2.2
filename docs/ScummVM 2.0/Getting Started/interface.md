---
title: Interface
nav_order: 4
parent: Quick Start
layout: default
---

# Interface
---

### The Launcher
This is the ScummVM main window, otherwise called "Launcher". You get to the Launcher whenever you start ScummVM without using command-line parameters to launch a game directly.

The big area on the left lists the games you have added to ScummVM. Besides showing the titles of those games, this list usually offers some additional information about each game, such as original platform, language, etc. You can highlight any game on the list by typing the first letter(s) of its title, or by simply clicking on it.

To the right of the list you can see a number of buttons. In brief, their functions are:  
- **Start** - launches the highlighted game
- **Load Game** - allows you to load a previously saved state for the highlighted game (if supported)
- **Add Game** - allows you to add a game to the list; when you press Shift, the Add Game button turns into Mass Add, which can be used to add several games in one go
- **Edit Game** - allows you to configure the highlighted game, overriding the global options
- **Remove Game** - removes the highlighted game from the list
- **Options** - allows you to configure global game settings, as well as a number of ScummVM options
- **About** - shows credits and miscellaneous information about your version of ScummVM
- **Quit** - closes the Launcher (quits the ScummVM application)

Just above the list of games, next to a magnifying glass icon, you can see a small input box. This is **Quick Search** - it allows you to filter your list of added games by a desired expression. For instance, you can type "Monkey Island" to quickly locate all "Monkey Island" games on the list, or you can type "German" if you wish to play a game in German - the uses are countless. There is no need for you to press anything to apply the filter you have typed: it is applied automatically on the fly. Also the filter is not case sensitive which means if you type "demo" it will display both the items that contain "demo" and those that contain "Demo". If you want to clear the filter and see the full list of your games, just press the **"C"** button next to the input box  

### Load Game
This menu allows you to run the highlighted game from a previously saved state straight from the Launcher, without having to start the game first. Here you can usually see the names of your savegames, their timestamps and screenshots to aid you in finding the exact state. When you have located the desired saved game, just select it and press Load to launch the game using that state. Besides loading a previous state, you can also delete obsolete saved games by highlighting them and clicking Delete.

Note that there are games that do not support this feature altogether, or whose saved states lack some information (e.g. playtime, screenshots).  

### Options
This menu allows you to define default game options, as well as change a number of the ScummVM Launcher's settings. For more details on how to fine-tune ScummVM and pre-configure games, see ["Configuring ScummVM"]({{ site.baseurl }}{% link docs/ScummVM 2.0/ScummVM Running Options/scummvm-running-options.md%}).

### Edit Game
You see this game configuration window whenever you add a game to the Launcher or click on Edit Game button. Here you can configure a game individually by overriding the default game settings you have set in the Launcher's Options, as well as change the game's language and original platform (if applicable). For more information, see ["Configuring a Game in ScummVM"]({{ site.baseurl }}{% link docs/ScummVM 2.0/Game Running Options/game-running-option.md%})

### Global Main Menu

The Global Menu (or GMM for Global Main Menu) is a feature that premiered in ScummVM 0.13.0. It is available in all games by pressing Crtl-F5 and provides the following features:

- **Resume**: close the GMM and resume the game.
- **Load**: load a game state (this is not available in all games).
- **Save**: save a game state (this is not available in all games).
- **Options**: change some options to play the game (e.g. music volume, subtitles speed).
- **About**: display the ScummVM About box (also available from the The Launcher).
- **Help**: displays a list of key commands (not available in all engines)
- **Return to Launcher**: quit the game and return to The Launcher (not available in all engines)
- **Quit**: quit the game and ScummVM and return to the Operating System.  

In some games you can still access the original menu by using Alt-F5. You can save and load games using this, however it is not intended for this purpose, and may even crash ScummVM in some games.