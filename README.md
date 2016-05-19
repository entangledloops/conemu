#A clean, Linux-like ConEmu (x64) configuration#

## Why use this? ##

Standard Command Prompt isn't for you, and you want some nice simple Linux behavior on your Windows machine.
For example, suppose you'd like a simple bash-like tabbed console emulator interface, that prints a standard `ls`
command like this:

![ls](http://www.entangledloops.com/img/ConEmu/ls.png)

And context menu integration in a slick little overhead, like this:

![Context](http://www.entangledloops.com/img/ConEmu/context.png)

![Mini](http://www.entangledloops.com/img/ConEmu/mini.png)

Out-of-the-box [ConEmu](https://conemu.github.io) is a great piece of software.
So is [GoW](https://github.com/bmatzelle/gow/wiki).
Although ConEmu comes prepackaged with [Clink](https://mridgers.github.io/clink), I'd suggest you grab the latest of that yourself too.

I've made some enhancements to the vanilla ConEmu settings that I think a wide audience might enjoy, if you're using a setup that involves these three components.

## Install ##

1) Download [ConEmu.xml](http://www.entangledloops.com/config/ConEmu.xml) by right-clicking and "Save as..."

2) In ConEmu settings (or upon install), choose "Import..." and select the file.

That's it!

## Notes ##

I've remapped my CapsLock key using the standard [scanmapset.exe](http://www.entangledloops.com/files/bin/scanmapset.exe) to F11.
That way, I just hit CapsLock and ConEmu appears. You can modify this in the keymaps however you want.

## Troubleshooting ##

Any "Specified path cannot be found"-like messages you encounter can be easily remedied by modifying any paths in the xml to match your own. There shouldn't be many, but there isn't any way to remove the ones I'm using and still show you how to find those options easily. Just use a text editor or the provided ConEmu settings menu if you need to adjust anything.