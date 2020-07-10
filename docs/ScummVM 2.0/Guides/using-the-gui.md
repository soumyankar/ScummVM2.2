---
layout: default
has_children: false
parent: Guides
title: Using the GUI
nav_order: 6
---

# Using the GUI

(_Screenshots wont load_)
The recommended way to use the tools are using the tool GUI, run the program tool program.

Most common usage is to compress files, to do that, simply click Next as compression is the default activity. If you are compressing Touche data files, you need to select advanced mode and then compress_touche, as the tools do not support selecting the touche directory automatically.

Next select the input file, depending on the tool you are using, this file to be selected differs greatly. You can look in the list below for the expected extension or filename, if you don't know it already. For some games this is obvious as there only is a single data file. For games that ship on multiple disks, select the first disk on this page, you will be asked for the second disk on the next page.

Sometime a tool is applied on a single file, but the game may contain many such file. By selecting Run on all files with the same extension you can automatically run the tool on all the files with the same extension and present in the same directory as the selected input file. For example you can run compress_scumm_san on all the SAN file of a game.

In most cases, the tool to be used will be automatically detected, if there are multiple options, you must manually select the correct tool to be used, this is usually obvious from the name of the tool, if you are unsure, check the list of tools below.

In this case, the correct tool (compress_queen) was automatically detected. Now select the output directory, note that the directory must exist. Extraction tools usually generate a large amount of output files, while compression tools generate a single archive. Since ScummVM usually expects a specific filename for compressed archives, you should not change the default after extraction completes.

Next, you will be asked for target platform. This is the platform that you are running ScummVM on, not the platform you are running the tools on. Note that this does not make the output files incompatible with other platforms. Instead it affects the default audio settings to be optimized for the platform selected, as support for some are very poor on certain platform (and will make ScummVM run very slow).

Next page asks audio for audio format to use, in most cases you can leave this at the default setting. If you want to configure bitrate and quality settings manually, check the advanced options checkbox, and you can change this at the next page.

After this, the tool will run. This can take a while and if all went well, you can continue on to the next page. If an error occured, you can go back to adjust settings. Take special care to note that some input files can cause the entire application to crash as many tools don't check too well for mal-formatted input files.

If all is well, advance to the next page to finish the guide! Enjoy your newly compressed/extracted data files!