---
title: "Using SVG2Mod to generate silkscreen images for KiCad from Inkscape"
description: "Sometimes you want more than just the default font."
categories:
 - electronics
tags:
 - electronics
 - kicad
 - inkscape
image: /images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/svgkicadsv2mod.png
---
Recently I've been working with [KiCad] to design some PCBs. On some of these I have added a small logo or mono image using the built in converter that comes with KiCad.  This tool allows you to take any image, colour or mono, and convert it into something you can add to your PCB.

Whilst this works the tool isn't great and does loose a significant amount of detail when converting things.

<img class="padded center"
        alt="Example of poor image quality from the KiCad converter"
        src="/images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/PoorImageQuality.png" />

For a recent project I wanted to make a face plate using a PCB as it's convenient, and should be pretty durable. Sadly the built in editor wasn't giving me results I was happy with for something that will be much more visible than normal.

Some research found a tool called [SVG2Mod](svg2mod) [^svg2mod1] which will convert an SVG into a .kicad_mod file that I can use.

<!-- more -->

## Installing SVG2Mod

You're going to need to use a command line, and Python3. If this means nothing to you then maybe time to stop reading.

I used [WSL] on Windows 10, but the same rough idea will work on linux and macOS.

First I needed Python3 and pip installed with the following command, macOS ships with Python 3 preinstalled so this isn't needed.

`sudo apt update`

`sudo apt install python3 python3-pip`

I also needed to close and reopen my terminal now for things to take.

Now install svg2mod using:

`pip3 install svg2mod`

Now we are ready to rock and roll.

## Using svg2mod

This is actually pretty simple, but you need to have your SVG drawn correctly. First only really paths are supported, theres "partial support" for rectangles and circles. The easiest thing to do is once you are happy with your design convert it all to paths using Path > Object to Path and Path > Stroke to Path.

This done run the tool and it will generate a mod file!

`svg2mod -i input.svg -p 1.0`

(run svg2mod for the input file input.svg with a precision of 1.0)

If you look at the [docs][svg2mod] there are lots of options you can use like -o for the output name or -c to set the 0,0 reference to the centre of the generated file.

## Fixing the errors

<img class="padded center"
        alt="Errors from converting an SVG with unsupported paths"
        src="/images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/ErrorMessages.png" />

Not just with A but a good example, 0 is the same as was a polarity symbol I drew.  

I used a font which was just the outlines, with no fill.  The way that the paths for this were generated caused an issue in svg2mod and so you will need to fix these.  The easiest way to find out what objects caused an error is to add the generated image to a pcb and see what isn't right.

This is a worked example to fix the 'a' I had.  This just a lower case which I ran Path > Object to Path on.  Red shows the stroke, black the fill.

<img class="padded center"
        alt="Lower case A showing the paths before fixing."
        src="/images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/A-outline.png" />

Select the affected object with the edit path tool (F2) and select Path > Break Apart.  Everything will probably go solid now and look horrid.

<img class="padded center"
        alt="Lower case A after using the break apart command"
        src="/images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/A-broken.png" />

To fix this you need to select the "pairs" of strokes that formed the shapes and then use Path > Difference. Do this for all objects and you will get a clean set of paths the tool can handle.

<img class="padded center"
        alt="Fixed lower case A after differencing the paths to resolve the nesting issue"
        src="/images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/A-fixed.png" />

This shows it in action and is probably far easier to follow.

<iframe width="560" height="315" src="https://www.youtube.com/embed/aaMOUHN18pM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Quality

The quality of this tool isn't perfect, but it can't be.  The pcb files can only handle so much precision and accuracy. The way it works is but creating lots of short straight lines to simulate curves, which when printed small on the PCB will look fine.

<img class="padded center"
        alt="Comparing the source SVG, KiCad conversion and svg2mod conversion"
        src="/images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/svgkicadsv2mod.png" />

You can see that the quality from the KiCad tool leaves a lot to be desired, but the svg2mod (-q 1.0) gives a very reasonable result.  Bare in mind these are going to be about 1.5mm tall when printed so we are very much zoomed in here.

svg2mod has a precision argument `-p`.  The default seems to be 10.0, and the example suggests 1.0 but there is no documentation on what the range is and what to expect to change.

<img class="padded center"
        alt="Comparison of -q settings 0.1 to 20.0"
        src="/images/2021-02-05-using-svg2mod-to-generate-silkscreen-images-for-kicad-from-inkscape/QualityComapre.png" />

I ran some tests lower values give higher quality. The lowest I tried was 0.1 and up to 20.0.  At 0.1 there was very minimal detail loss, which creeps in at 1.0 and by 20.0 is a little more noticeable.  Even with this said you can only see this when zoomed right in, 1000% or so is what I am using to look at these differences.  At 100% scale all of this is academic.  If you're struggling to see the difference you can see the rounded corner at the bottom of the + become more straight edge chamfers.

Given the size that these will be rendered at 1.0 is probably the correct value.  However 0.1 doesn't seem to slow down the software so perhpase it's worth trying just to give the best possible result.

[^svg2mod1]: Note this isn't the original version, but a fork.  The original version is now no longer maintained but this version is.

[KiCad]: https://kicad.org
[svg2mod]: https://github.com/svg2mod/svg2mod
[WSL]: https://docs.microsoft.com/en-us/windows/wsl/install-win10
[Homebrew]: https://brew.sh
