#A clean, Linux-like ConEmu (x64) configuration#

- [Why Use This?](#why-use-this)
- [Install](#install)
- [Notes](#notes)
- [Troubleshooting](#troubleshooting)

## Why use this? ##

My configuration normalizes behavior to a Linux-like mode for a modern x64-based machine, adjusting the copious available settings options to veteran expectations. There are numerous checkboxes and tooltips, and experimenting with the settings is the only true way to elucidate some of the behavior described by the authors. 

**Here is a very incomplete list of some of the changes off the top of my head:**

- key remaps improved to keep you sane and learning curve at a low and accidents minimized (e.g. standard terminal window/tab management shortcuts such as Ctrl+PgUp, etc.; remaps WinKey -> Ctrl in some instances for universal compat. and/or more frequently used options; extraneous remaps for rarely used options removed to prevent accidents; laptops accounted for by removing Fn-key / numpad dependent behavior; many others)
- ESC acts as instant-hide for ConEmu window; shift+ESC for process-defined behavior (i.e. ordinary behavior)
- colors corrected for standard terminal compatability
- instant-terminal via F11, which I've personally remapped CapsLock to; change at will
- all terminals will share the same ConEmu instance, but use different tabs which can be pulled out if desired
- double-click a tab for a settings-identical clone; left ctrl + double-click to kill a tab
- proper key handling w/provided overrides for escaping characters, multiline paste, and other associated term-like behavior
- disables all audio bells
- fonts rendered nicely and sized for maximum readable content based on resolution (where possible; overrides available via keymaps)
- first-time run prompts disabled
- icon added to tray so you know if you have an instance started
- context menu integration ("ConEmu Here" + an admin version)

For example, suppose you'd like a simple bash-like tabbed console emulator interface, that prints a standard `ls`
command like this:

![ls](http://www.entangledloops.com/img/ConEmu/ls.png)

And context menu integration in a slick little overhead, like this:

![Context](http://www.entangledloops.com/img/ConEmu/context.png)

![Mini](http://www.entangledloops.com/img/ConEmu/mini.png)

Out-of-the-box [ConEmu](https://conemu.github.io) is a great piece of software.
So are [GoW](https://github.com/bmatzelle/gow/wiki) and [Clink](https://mridgers.github.io/clink).

I've made some enhancements to the vanilla ConEmu settings that I think a wider audience might enjoy, if you're using a setup that involves these three components.

## Install ##

1. Download and extract clink into `ConEmu\ConEmu\clink` as described in the `Readme.txt` file in the same folder.
2. In ConEmu settings (or upon install), choose "Import..." and select the file.
3. If you get a warning about "On Top", you can safely ignore and **select "no" if  asked to revert**.
4. Close and reopen ConEmu.

#### Optional ####

If you'd like an instance to spawn quietly in the background at system startup so you can just hit CapsLock (or your remap) to enter a drop-down terminal:

1. Press WinKey + R (should open Run dialog).
2. Type `shell:startup` and hit enter.
3. In the folder, right-click and Create Shortcut to ConEmu64 executable.
4. Right-click shortcut, properties, and set target like this:

      `"C:\path\to\your\ConEmu64.exe" -FS -Max -StartTSA`

Those options start ConEmu in fullscreen, maximized, and in the background iconified to tray.

## Notes ##

Last tested for compatability with **ConEmu 160592 [Preview]**.

I've remapped my CapsLock key using the standard [scanmapset.exe](http://www.entangledloops.com/files/bin/scanmapset.exe) to F11.
That way, I just hit CapsLock and ConEmu appears. You can modify this in the keymaps however you want.

## Troubleshooting ##

If context menu integration is missing, you may have click the button "Register" buttons one time each found under:

    Settings -> Integration

Any "Specified path cannot be found"-like messages you encounter can be easily remedied by modifying any paths in the xml to match your own. There shouldn't be many, but there isn't any way to remove the ones I'm using and still show you how to find those options easily. Just use a text editor or the provided ConEmu settings menu if you need to adjust anything.
