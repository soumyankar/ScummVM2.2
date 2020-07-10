---
layout: default
parent: ScummVM Configuration
title: Configuration File
has_children: true
nav_order: 3
---

# Configuration File

The configuration file stores the settings that have been saved on the ScummVM GUI. This is a plain text file which can be edited directly. 

There are some **advanced settings which are only available through the configuration file only.**

## Config file location path

| Operating System    |      Location of config file                 |
|:--------|:-------------------------------|
| Windows Vista	 | \Users\username\AppData\Roaming\ScummVM\scummvm.ini|
| Windows 2000/XP  | \Documents and Settings\username\Application Data\ScummVM\scummvm.ini |
| Windows NT4 | <windir>\Profiles\username\Application Data\ScummVM\scummvm.ini|
| Windows 95/98/ME | <windir>\scummvm.ini |
| Unix | $HOME/.scummvmrc |
| Mac OS X | $HOME/Library/Preferences/ScummVM Preferences |
| Others | scummvm.ini in the current directory |	

## Config file description

Normally, ScummVM’s configuration file does not need to be modified directly, as all options are adjustable from the ScummVM GUI. However, there are some advanced options only available by editing the configuration file directly:  

| INI    |     Name                 |                  Description                 |
|:--------|:-------------------------------|:--------------------------------------|
| scummvm	 | output_rate | Overrides the audio output sampling frequency. The default value is 44100. See the Music and sound appendix for some guidelines on good values to use. |
| scummvm	 | audio_buffer_size | Overrides the size of the audio buffer. This can be decreased if audio latency is high, or increased if audio drop-outs are experienced. The value must be one of: 256 512 1024 2048 4096 8192 16384 32768. The default value is calculated based on output sampling frequency to keep audio latency below 45ms. (since 2.0) |
| scummvm	 | joystick_num | Number of joystick device to use for input. |
| scummvm	 | last_fullscreen_mode_width
last_fullscreen_mode_height |Specify the resolution to use on fullscreen when using the OpenGL graphics mode. This is used internally to remember the last resolution used, and reuse it the next time we go to fullscreen. This can also be set manually to a desired fullscreen resolution. |
| scummvm	 | disable_display | Can be used to disable display when replaying events using the event recorder. |
| scummvm	 | screenshotpath | Indicate the path where to saved the screenshot. The default is system-dependent. |
| scummvm	 | iconspath | Indicate the path where to look for game icons for task bar integration on Windows and macOS X. The game icons are used as overlay for the ScummVM icon in the taskbar / Dock when a game is running. The icons files should be named after the game ids and be .ico on Windows and .png on macOS X. |
| scummvm	 | console | Enable or disable the console on Windows. By default it is enabled. |