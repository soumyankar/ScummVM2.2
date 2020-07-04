---
layout: default
parent: Advanced Configuration
grand_parent: ScummVM Configuration
title: Graphics Filters
nav_order: 2
---

# Graphics Filters

ScummVM offers several anti-aliasing filters to attempt to improve visual quality. These filters take the original game graphics, and scale it by a certain fixed factor (usually 2x or 3x) before displaying them to you. So for example, if the game originally ran at a resolution of 320x200 (typical for most of the SCUMM games), then using a filter with a scale factor of 2x will effectively yield 640x400 graphics. Likewise a 3x filter will give 960x600.

ScummVM uses the following graphic filters:

1. The different scale factors and what they do.
1. Command line option.
1. Notes.