---
layout: default
parent: Configuration File
grand_parent: ScummVM Configuration
title: Engine-Specific
nav_order: 3
---

# Engine Specific Settings

### Sierra games using the AGI engine

Sierra games using the AGI engine adds the following non-standard keywords:

```
originalsaveload   bool     If true, the original save/load screens are
                            used instead of the enhanced ScummVM ones
altamigapalette    bool     Use an alternative palette, common for all
                            Amiga games. This was the old behavior
mousesupport       bool     Enables mouse support. Allows to use mouse
                            for movement and in game menus
```

### Sierra games using the SCI engine

Sierra games using the SCI engine adds the following non-standard keywords:

```
disable_dithering  bool     Remove dithering artifacts from EGA games
prefer_digitalsfx  bool     If true, digital sound effects are preferred
                            instead of synthesized ones
originalsaveload   bool     If true, the original save/load screens are
                            used instead of the enhanced ScummVM ones
native_fb01        bool     If true, the music driver for an IBM Music
                            Feature card or a Yamaha FB-01 FM synth module
                            is used for MIDI output
use_cdaudio        bool     Use CD audio instead of in-game audio,
                            when available
windows_cursors    bool     Use the Windows cursors (smaller and monochrome)
                            instead of the DOS ones (King's Quest 6)
silver_cursors     bool     Use the alternate set of silver cursors,
                            instead of the normal golden ones (Space Quest 4)
```                                                        