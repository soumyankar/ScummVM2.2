---
layout: default
parent: ScummVM Configuration
title: Command Line
nav_order: 2
---

# Command Line Options

ScummVM can be accessed through the command line. This section talks about the different command line options. The meaning of most long options (that is, those options starting with a double-dash) can be inverted by prefixing them with "no-". For example, ```--no-aspect-ratio``` will turn aspect ratio correction off. This is useful if you want to override a setting in the configuration file.

The short game name ('game target') you see at the end of the command line specifies which game is started. It either corresponds to an arbitrary user defined target (from the configuration file), or to a built-in gameid.

```
Usage: scummvm [OPTIONS]... [GAME]

[GAME]                   Short name of game to load. For example, 'monkey'
                          for Monkey Island. This can be either a built-in
                          gameid, or a user configured target.

-v, --version            Display ScummVM version information and exit
-h, --help               Display a brief help text and exit
-z, --list-games         Display list of supported games and exit
-t, --list-targets       Display list of configured targets and exit
--list-saves             Display a list of saved games for the target specified
                          with --game=TARGET, or all targets if none is specified
-a, --add                Add all games from current or specified directory.
                          If --game=ID is passed only the game with id ID is
                          added. See also --detect.
                          Use --path=PATH to specify a directory.
--detect                 Display a list of games with their ID from current or
                          specified directory without adding it to the config.
                          Use --path=PATH to specify a directory.
--game=ID                In combination with --add or --detect only adds or attempts to
                          detect the game with id ID.
--auto-detect            Display a list of games from current or specified directory
                          and start the first one. Use --path=PATH to specify
                          a directory.
--recursive              In combination with --add or --detect recurse down all
                          subdirectories
--console                Enable the console window (default: enabled) (Windows only)

-c, --config=CONFIG      Use alternate configuration file
-p, --path=PATH          Path to where the game is installed
-x, --save-slot[=NUM]    Saved game slot to load (default: autosave)
-f, --fullscreen         Force full-screen mode
-F, --no-fullscreen      Force windowed mode
-g, --gfx-mode=MODE      Select graphics scaler (see also section 5.3)
--stretch-mode=MODE      Select stretch mode (center, integral, fit, stretch)
--filtering              Force filtered graphics mode
--no-filtering           Force unfiltered graphics mode


--gui-theme=THEME        Select GUI theme (default, modern, classic)
--themepath=PATH         Path to where GUI themes are stored
--list-themes            Display list of all usable GUI themes
-e, --music-driver=MODE  Select music driver (see also section 7.0)
--list-audio-devices     List all available audio devices
-q, --language=LANG      Select game's language (see also section 5.5)
-m, --music-volume=NUM   Set the music volume, 0-255 (default: 192)
-s, --sfx-volume=NUM     Set the sfx volume, 0-255 (default: 192)
-r, --speech-volume=NUM  Set the voice volume, 0-255 (default: 192)
--midi-gain=NUM          Set the gain for MIDI playback, 0-1000 (default: 100)
                          (only supported by some MIDI drivers)
-n, --subtitles          Enable subtitles (use with games that have voice)
-b, --boot-param=NUM     Pass number to the boot script (boot param)
-d, --debuglevel=NUM     Set debug verbosity level
--debugflags=FLAGS       Enable engine specific debug flags
                          (separated by commas)
-u, --dump-scripts       Enable script dumping if a directory called 'dumps'
                          exists in the current directory

--cdrom=NUM              CD drive to play CD audio from (default: 0 = first
                          drive)
--joystick[=NUM]         Enable joystick input (default: 0 = first joystick)
--platform=WORD          Specify platform of game (allowed values: 2gs, 3do,
                          acorn, amiga, atari, c64, fmtowns, mac, nes, pc,
                          pce, segacd, windows)
--savepath=PATH          Path to where saved games are stored
--extrapath=PATH         Extra path to additional game data
--soundfont=FILE         Select the SoundFont for MIDI playback (Only
                          supported by some MIDI drivers)
--multi-midi             Enable combination of AdLib and native MIDI
--native-mt32            True Roland MT-32 (disable GM emulation)
--enable-gs              Enable Roland GS mode for MIDI playback
--output-rate=RATE       Select output sample rate in Hz (e.g. 22050)
--opl-driver=DRIVER      Select AdLib (OPL) emulator (db, mame, nuked)
--aspect-ratio           Enable aspect ratio correction
--render-mode=MODE       Enable additional render modes (hercGreen, hercAmber,
                          cga, ega, vga, amiga, fmtowns, pc9821, pc9801, 2gs,
                          atari, macintosh)

--alt-intro              Use alternative intro for CD versions of Beneath a
                          Steel Sky and Flight of the Amazon Queen
--copy-protection        Enable copy protection in games, when
                          ScummVM disables it by default.
--talkspeed=NUM          Set talk delay for SCUMM games, or talk speed for
                          other games (default: 60)
--demo-mode              Start demo mode of Maniac Mansion (Classic version)
--tempo=NUM              Set music tempo (in percent, 50-200) for SCUMM games
                          (default: 100)
```

Examples:  

- Win32: Running Monkey Island, fullscreen, from a hard disk: ```C:\Games\LucasArts\scummvm.exe -f -pC:\Games\LucasArts\monkey\ monkey```  
Running Full Throttle from CD, fullscreen and with subtitles enabled: C:\Games\LucasArts\scummvm.exe -f -n -pD:\resource\ ft  
- Unix: Running Monkey Island, fullscreen, from a hard disk: ```/path/to/scummvm -f -p/games/LucasArts/monkey/ monkey```  
Running Full Throttle from CD, fullscreen and with subtitles enabled: ```/path/to/scummvm -f -n -p/cdrom/resource/ ft```

