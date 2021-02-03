---
title: "Using SVG2Mod to generate silkscreen images for KiCad from Inkscape"
description: "Sometimes you want more than just the default font."
categories:
 - electronics
tags:
 - electronics
 - kicad
 - inkscape
image: 
---
Recently I've been working with [KiCad] to design some PCBs. On some of these I have added a small logo or mono image using the built in convertor that comes with KiCad.  Depsite some of these logo's not being drawn in Inkscape to use this method you will need to. as it will comvert an SVG to the KiCad format.

Whilst this works the tool isn't great and does loose a significant amount of detail when converting things.

{Example of bad quality}

For a recent project I wanted to make a face plate using a PCB as it's convenient, and should be pretty durable. Sadly the built in editor wasn't giving me results I was happy with.

Some research found a tool called [SVG2Mod][^svg2mod1] which will convert an SVG into a .kicad_mod file that I can use.

## Installing SVG2Mod

You're going to need to use a command line, and Python3. If this means nothing to you then maybe time to stop reading.

I used [WSL] on Windows 10, but the same rough idea will work on linux and macOS.

First I needed Python3 and pip installed with the following command (on macOs you will probably need to use [Homebrew])

`sudo apt update`

`sudo apt install python3 python3-pip`

I also needed to close and reopen my terminal now for things to take.

Now install svg2mod using:

`pip3 install svg2mod`

There was some fiddling with paths but I think this is all actually managed for you, just open a new terminal to force things to reload.

## Using svg2mod

This is actually pretty simple, but you need to have your SVG right. First only really paths are supported, theres "partial support" for rectangles and circles. The easiest thing to do is once you are happy with your design convert it all to paths using Path > Object to Path and Path > Stroke to Path.

This done run the tool and it will generate a mod file!

`svg2mod -i input.svg -p 1.0`

(run svg2mod for the input file input.svg with a precision of 1.0)

If you look at the link above there are lots of options you can use like -o for the output name or -c to set the 0,0 reference to the centre.

## The letter A

{errors}

Not just with A but a good example, 0 is the same as was a polarity symbol I drew.  

I used a font which was just the outlines, with no fill.  The way that the paths for this were genrated casused an issue in svg2mod and so you will need to fix these.  The easiest way to find out what objects caused an errorr is to add the genrated image to a pcb and see what isn't right.

This is a worked example to fix the 'a' I had.  This just a lower case which I ran Path > Object to Path on.  Red shows the stroke, black the fill.

{A}

Select the affected object with the edit path tool (F2) and select Path > Break Apart.  Everything will probably go solid now and look horrid.

{A broken}

To fix this you need to select the "pairs" of strokes that formed the shapes and then use Path > Difference. Do this for all objects and you will get a clean set of paths the tool can handle.

{A fixed}

This shows it in action and is probably far easier to follow.

<iframe width="560" height="315" src="https://www.youtube.com/embed/aaMOUHN18pM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Quality

The quality of this tool isn't perfect, but it can't be.  The pcb files can only handle so much precision and accuracy. The way it works is but creating lots of short straight lines to simulate curves, which when printed small on the PCB will look fine.

{svg|kicadtool|svg2mod}

svg2mod has a precision argument `-p`.  The default seems to be 10.0, and the example suggests 1.0.  Precisions of > 1.0 seem to all be essenittially the same <0.1 greater detial.  make a swatch 0.1, 0.5, 1, 10 ,20


[^svg2mod1]: Note this isn't the original version, but a fork.  The original version is now no longer maintained but this version is.

[KiCad]: https://kicad.org
[SVG2Mod]: https://github.com/svg2mod/svg2mod
[WSL]: https://docs.microsoft.com/en-us/windows/wsl/install-win10
[Homebrew]: https://brew.sh