---
layout: default
title: Solution
nav_order: 2
description: "Proposal for Google Season of Docs '20 on ScummVM"
permalink: /solution
---

# Solution

The new documentation portal will not carry forward the mistakes previously made. This section will talk about my approach towards making this project a success; The solution has been formulated keeping everything in mind that was discussed on the previous page. The key points of the new documentation are summarized as follows:

1. Collecting and Gathering
	- Information will be gathered from the User Manual, Wiki, and README to create the new portal. The guides will be written by **coalescing only the essential bits of information**. The new content would be brief for the beginner user and engaging to the veteran.
	- **Features will not be seen zoned anymore**. Certain features are of necessity to the user but are prone to be overlooked. The new documentation portal will showcase all the functionalities of ScummVM.
	- **No repetitions**. All relevant content should be in one spot. A complete compilation of all the resources in one portal. No more dispersion of data.
    - **Improved flow of information**. Information has been re-written after collecting. Consistency has been maintained to reflect a feel of a course.
1. Better support
	- **Refreshing the manuals**. The current manual is good but has become outdated. Individual sections of documentation need prime focus, such as: Running options, Configuration. These documents need to be dusted and filtered off of the unnecessary.
	- **Scattered help**. ScummVM has documented specific commonly faced issues, but again, they are all over the place. For instance: FAQs exist on every document portal. They need to be compiled and shown in one spot, preferably with tags.
1. **Brand new layout**
	- I have compiled the entire sitemap of the new documentation portal. This will highlight all the significant changes between the existing user manual and my portal. **Relocation of information is vital** and one of the primary goals would be to keep resources where they should be.
	- Divided section "_Using ScummVM_" into 2 parts - "_ScummVM Running Options" and "_Game Running Options_". This was done to improve readability and achieving the objective of assembling resources.
    - "_ScummVM Running Options_" focuses on the application and all related functions.
    - "_Game Running Options_" focuses on games, their issues, and related functions. 
	- Added new sections:
		- "_Guides_": Features of ScummVM that every beginner and intermediate user would be interested in. (Command line options, Installation guides etc. ). This section gives prime focus towards hands-on knowledge about ScummVM. Users will find it extremely helpful 
		- "_Advanced Guides_": Features of ScummVM that only the experts use. (Compiling binaries, Music and Sound etc.) 
	- Removed section "_ScummVM Interface_". 

## Proposed Sitemap

```
├── Game\ Running\ Options
│   ├── controls.md
│   ├── custom-options.md
│   ├── game-running-option.md
│   ├── hotkeys.md
│   ├── installing-games.md
│   ├── playing-a-game.md
│   └── removing-games.md
├── Getting\ Help
│   ├── changelog.md
│   ├── contact.md
│   ├── credits.md
│   ├── faq.md
│   ├── getting-help.md
│   ├── reporting-bugs.md
│   └── translations.md
├── Getting\ Started
│   ├── configuration.md
│   ├── getting-started.md
│   └── installation.md
├── Guides
│   ├── cloud-and-lan.md
│   ├── guides.md
│   ├── save-files.md
│   └── screenshots.md
├── Introduction
│   └── introduction.md
└── ScummVM\ Running\ Options
    ├── Advanced\ Guides
    │   ├── command-line.md
    │   ├── configuration-file.md
    │   ├── graphics-filters.md
    │   └── music-and-sound.md
    ├── Obtaining\ ScummVM
    │   ├── amiga-os4.md
    │   ├── atari.md
    │   ├── beos.md
    │   ├── debian.md
    │   ├── macos.md
    │   └── windows.md
    ├── advanced-guides.md
    ├── configuring.md
    ├── obtaining-scummvm.md
    ├── platforms.md
    ├── requirements.md
    ├── scummvm-running-options.md
    └── uninstalling.md

8 directories, 39 files
```

- [Read Work Plan]({{ site.baseurl }}{% link work-plan.md%})