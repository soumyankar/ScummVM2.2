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
1. Hierarchy improvement
    - **Facilitating the information**. Certain sections of the documentation lack proper arrangment. For instance: command-line options. It should be divided into groups; General, configuration, save-files, music etc. I have tried to present an example [here]({{ site.baseurl }}{% link docs/ScummVM 2.0/ScummVM Running Options/command-line.md%})
    - **Step-by-step approach**. Information should be supplied in a layered, top-down approach. The existing documentation has been broken down and divided into groups for a better outlook.
1. **Brand new layout**
	- I have compiled the entire sitemap of the new documentation portal. This will highlight all the significant changes between the existing user manual and my portal. **Relocation of information is vital** and one of the primary goals would be to keep resources where they should be.
	- Divided section "_Using ScummVM_" into 2 parts - "_ScummVM Running Options" and "_Game Running Options_". This was done to improve readability and achieving the objective of assembling resources.
    - "_ScummVM Running Options_" focuses on the application and all related functions.
    - "_Game Running Options_" focuses on games, their issues, and related functions. 
	- Added new sections:
		- "_Guides_": Features of ScummVM that every beginner and intermediate user would be interested in. (Command line options, Installation guides etc. ). This section gives prime focus towards hands-on knowledge about ScummVM. Users will find it extremely helpful 
		- "_Advanced Configuration_": Features of ScummVM that only the experts use. (Compiling binaries, Music and Sound etc.) 
	- Removed section "_ScummVM Interface_". 
    - Created separate sections to achieve better organising of docs.

## Proposed Sitemap

```bash
├── Game\ Installation
│   ├── game-installation.md
│   ├── game-specific-instructions.md
│   ├── general-instructions.md
│   └── port-specific-instructions.md
├── Game\ Notes
│   └── game-notes.md
├── Game\ Running\ Options
│   ├── custom-options.md
│   ├── game-running-option.md
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
│   ├── installation.md
│   ├── interface.md
│   ├── quick-start.md
│   └── requirements.md
├── Guides
│   ├── boot-params.md
│   ├── cloud-and-lan.md
│   ├── compiling-from-source.md
│   ├── guides.md
│   ├── save-files.md
│   ├── screenshots.md
│   ├── using-the-cli.md
│   └── using-the-gui.md
├── Introduction
│   └── introduction.md
├── Running\ ScummVM
│   ├── controls-and-mapping.md
│   ├── hotkeys.md
│   ├── language-options.md
│   └── running-scummvm.md
├── ScummVM\ Running\ Options
│   ├── advanced-configuration.md
│   ├── command-line.md
│   ├── configuration-file.md
│   ├── engine-specific-settings.md
│   ├── game-configuration-settings.md
│   ├── general-configuration-file-settings.md
│   ├── graphics-filters.md
│   ├── launcher.md
│   ├── music-and-sound.md
│   ├── render-modes.md
│   ├── scummvm-running-options.md
│   └── uninstalling.md
├── Supported\ Games
│   ├── activision.md
│   ├── adventuresoft.md
│   ├── animation-magic.md
│   ├── coktel-vision.md
│   ├── humongous.md
│   ├── living-books.md
│   ├── lucasarts-scumm.md
│   ├── not-completable.md
│   ├── others.md
│   ├── revolution-games.md
│   ├── sierra-sci.md
│   ├── sierra.md
│   └── supported-games.md
└── Troubleshooting
    ├── engine-specific.md
    ├── game-specific.md
    ├── loom-tg-16.md
    ├── mac-games.md
    └── troubleshooting.md

11 directories, 62 files

```

- [Read Work Plan]({{ site.baseurl }}{% link work-plan.md%})