---
layout: default
parent: Advanced Configuration
grand_parent: ScummVM Configuration
title: Render Modes
nav_order: 3
---

# Render Modes

For most games this will have no impact. For some of the older games that could be played on different systems / graphics cards, this control allows us to decide which system we want ScummVM to reproduce. The options are:

- default

- Hercules Green

- Hercules Amber

- CGA (4 colors)

- EGA (16 colors)

- Amiga (32 colors)

To select a render mode from the command line, use the ```'--render-mode'``` option (see Command line options), e.g.:

```scummvm --render-mode=CGA maniac```