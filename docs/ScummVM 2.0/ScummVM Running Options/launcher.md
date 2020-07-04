---
layout: default
title: Launcher Configuration
parent: ScummVM Configuration
nav_order: 1
---

# Launcher Configuration

The ScummVM Launcher gives us a graphical method for changing the settings that it uses to run games. There are two ways to do this: firstly by changing the default settings (which games will follow unless told otherwise), secondly by configuring an individual game to use settings that are different from the defaults. To begin with we will look at changing the default settings. To do this, click on the "Options" button on the right-hand side of the Launcher window. There are many options, and they are separated into tabs: we shall look at each tab in turn.

### Graphics Tab

The graphics tab allows us to change various things about the way the games are displayed on screen when played.

| Control    |      Description                 |
|:--------|:-------------------------------|
| Graphics Mode | This allows us to change the graphic filter that ScummVM uses (e.g. to scale the game to a bigger resolution). The option has no effect on games whose original resolution is higher than 320x200 or 320x240 (e.g. 640x480) - such games should be configured separately. See the Graphic filters section of the manual for more detail              |
| Render Mode  | This allows us to change the render mode that ScummVM uses. See the Render Modes section of the manual for more detail              |
| Aspect Ratio correction  | Most games supported by ScummVM were designed to be played at a screen resolution of 320x200 using rectangular pixels (higher than they were wide). Most modern systems however are using square pixels, which means that the image appears to be squeezed vertically and the characters look wider and shorter than they should. If this option is checked, ScummVM corrects for this by stretching the game window to a resolution of 320x240 which with square pixels looks the same as 320x200 on old monitors. As with Graphic filters, this takes a little processing power to achieve. We can combine this with a Graphic filter, and for example with a scaling of x2 the window size will be 640x480 instead of 640x400.                |
| Fullscreen mode  | Switches between playing games in a window, or playing them in fullscreen mode. Switch between the two using Alt-Enter while in a game.                 |

### Audio Tab

The audio tab in the options allows us to change various things about the way that sound is outputted in ScummVM games.

| Control    |      Description                 |
|:--------|:-------------------------------|
| Music Driver | This is the method that ScummVM uses to output MIDI music. For more details, see the section on music drivers.              |
| AdLib Emulator  | This is the emulator used by ScummVM to generate the music when the AdLib music driver is selected. Two emulators are currently available. MAME OPL emulator was the emulator that was used up to version 0.13.1. More recently the DOSBox OPL emulator has been added (but is still experimental).              |
| Output Rate | This is the sample rate at which ScummVM plays back sounds (including music if using an emulation music driver, such as the AdLib music driver). For more information, see the Output sample rate section                |
| Subtitle Speed | This allows the user to adjust the length of time that the subtitles are displayed on screen: the lower the speed is set, the longer the subtitles appear for.                 |

### Volume Tab

The volume tab allows us to set the relative volumes for the various different types of sound that ScummVM plays.

| Control    |      Description                 |
|:--------|:-------------------------------|
| Music Voume | The volume of the music played back in games. This is usually MIDI music played back with one of the music drivers, but some games use digitized music.|
| SFX Volume  | The volume of the sound effects within the games.|
| Speech Volume | The volume of the digitized speech in the game, if it has any.|
| Mute All | Mute all sounds.|

### MIDI Tab

The MIDI tab lets us change various settings about the MIDI music played back in games.

| Control    |      Description                 |
|:--------|:-------------------------------|
| Soundfont | Some music drivers require you to provide them with a Soundfont, which contains samples of instruments for the device to play back. This setting allows you to choose one.|
| Mixed AdLib/MIDI mode  | Some games contain sound effects that are exclusive to the AdLib soundtrack. For these games, you may wish to use this mode in order to combine MIDI music with AdLib sound effects.|
| True Roland MT-32 (disable GM emulation) | ScummVM will treat your device as a real MT-32. Because the instrument mappings and system exclusive commands of the MT-32 vary from those of General MIDI devices, you should only enable this option if you are using an actual Roland MT-32, LAPC-I, CM-64, CM-32L, CM-500, or GS device with an MT-32 map.|
| Enable Roland GS Mode | ScummVM will initialize your GS-compatible device with settings that mimic the MT-32's reverb, (lack of) chorus, pitch bend sensitivity, etc. If it is specified in conjunction with True Roland MT-32 (above), ScummVM will select the MT-32-compatible map and drumset on your GS device. This setting works better than default GM or GS emulation with games that do not have custom instrument mappings (Loom and The Secret of Monkey Island). You should only specify both settings if you are using a GS device that has an MT-32 map, e.g. SC-55, SC-88, SC-8820, etc. Please note that Roland GS Mode is automatically disabled in both Day of the Tentacle and Sam & Max Hit the Road, since they use General MIDI natively. If neither of the above settings is enabled, ScummVM will initialize your device in General MIDI mode and use GM emulation in games with MT-32 soundtracks.|
| MIDI gain | The relative volume of the general MIDI music. This is only supported by some of the music drivers.|

### Paths Tab

This part of the options lets the user tell ScummVM where to look for particular files.  


| Control    |      Description                 |
|:--------|:-------------------------------|
| Save Path | This is the default folder in which ScummVM will store saved games. If this is not set, saved games will generally be stored in the current directory. Exceptions to this include:  |
| Speech Volume | The volume of the digitized speech in the game, if it has any.|
| Mute All | Mute all sounds.|

### Misc Tab

The Misc tab contains options that don't belong on any of the other tabs

| Control    |      Description                 |
|:--------|:-------------------------------|
| Theme | Click on this button to change the visual appearance of the ScummVM Launcher|
| GUI Renderer  | This settings defines how the ScummVM GUI is rendered. The two options are to use either the normal renderer or an antialiased renderer.|
| Autosave |In some games (namely Beneath a Steel Sky, Flight of the Amazon Queen and all SCUMM games), ScummVM will automatically save the game every few minutes. For the SCUMM engine, it will save in Slot 0. This saved game can be loaded again using Ctrl-0 or the F5 menu. Use this control to adjust the time period that ScummVM waits between saves; the default setting is 5 minutes.|

### Custom game options that can be toggled via the GUI 

A lot of the custom game options in the previous section can be toggled via the GUI. If a custom option is available for a specific game, a new tab called "Engine" will appear when adding or editing the configuration of that game. If the custom options are not shown, the games in question will need to be run once or readded in the ScummVM launcher's game list. This will update the configuration of each entry, allowing the custom options to be shown.

#### Engine Tab

A lot of the custom game options in the previous section can be toggled via the GUI. If a custom option is available for a specific game, a new tab called "Engine" will appear when adding or editing the configuration of that game. If the custom options are not shown, the games in question will need to be run once or readded in the ScummVM launcher's game list. This will update the configuration of each entry, allowing the custom options to be shown.
Read the next section to read about command-line options.