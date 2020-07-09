---
layout: default
has_children: false
parent: Guides
title: Screenshots & Icons
nav_order: 2
---

# Screenshots

On systems using the SDL backend(for example, Windows, Mac, or Linux) you can use ```alt+s``` to take snapshots.

You can specify the directory in which you want the screenshots to be created in the config file. To do so add a screenshotpath value under the [scummvm] section:

```
[scummvm]
screenshotpath=/path/to/screenshots/
```

The default location, when no screenshot path is defined in the config file, depends on the OS:

- Windows: In ```Users\username\My Pictures\ScummVM Screenshots```.
- macOS X: On the Desktop.
- Other unices: In the XDG Pictures user directory, e.g. ```~/Pictures/ScummVM Screenshots```
- Any other OS: In the current directory.

### How to make screenshots

Here are additional rules on how to make screenshots which were settled in the last couple of years: (Of course any suggestions are welcome!)

- Check if this particular screenshot hasn't already been committed.
	- If there is no visual difference between an already submitted screenshot and your game version, don't submit it.
	- If you are submitting screenshots for non-English game, use only those which have visual difference (changed graphics) or have something written in that language.
- ScummVM settings
	- Pick an interesting scene to take the screenshot of.
	- 320x200 games should be run with HQ2x (Ctrl+Alt+3) mode and with aspect correction (Ctrl+Alt+a) mode on. I.e. it should be a 640x480 image.
	- 640x480 games should be run without a scaler.
	- On platforms which use the SDL backend (Win32 and _*_ nix included) Alt+S creates a screenshot file called scummvmXXXXX.png inside the screenshot directory. The default location for screenshots depends on the OS. See the README.md for details.
	- Make sure your screenshot is at least 640x480 and was made with HQ2x scaler (if originally 320x200). Otherwise it won't be accepted.
	- If the game runs at a different resolution (such as 512x384, or 800x600), use the normal mode (no scaling) and make sure your screenshot is at the original resolution.

(TODO, missing info.)

### How to make game icons
On screenshots page you may see the set of nice 'headshots' used for the games. If you are submitting screenshots for a new game, you may help with creating the icon too.

**Don'ts:**

	1. Use an image that has been scaled up with a filter
	1. Avoid scaling down unless absolutely necessary, if you do scale down, always scale proportionally and try both Nearest Neighbor or Lancoze to see what looks better
	1. Keep shadows. Shadows will be done dynamically in CSS.

**Dos:**

	1. Start with our icon template to frame your icon. The image should be centered on the white dot and never flow outside the black rectangle.
	1. Be creative
	1. Pick a distinguishable image from the game or series. Either a sprite of the main character, a portrait, or a recognizable item/icon from the game
	1. Scale up as needed. Only scale up in 2x increments using Nearest Neighbor to preserve pixel art
	1. Have sprites and portraits face to the right
	1. Erase necessary pixels around the object

### How to submit screenshots

- If you have write access to our web source repository, you can commit it directly to the relevant directory.
- Alternatively, you can submit it via our bug tracker.
	- There is a restriction on 250kb per file. There are 2 options you can do:
		- Submit several files (you may add them one by one)
		- Upload somewhere in one archive and provide link in the bugreport
- If you didn't perform some actions with the screenshot file, for example if you didn't compress it or were unable to produce thumbnails, please mark your submission accordingly.
- Save the result as PNG
