---
title: "MP38A Germanium NPN Transistor Pin Out"
description: "Some nerdy stuff about vintage electronic components from the USSR"
categories:
 - electronics
tags:
 - transistor
 - npn
 - germanium
 - datasheet
---
I've recently been working on a DIY guitar effects pedal.  A lot of these use old vintage parts long since replaced as they are designs from the 60s.  This means finding suitable bits on eBay.

Most of the old British/American parts are highly desirable, hard to find and so expensive.  What are still pretty easy to get hold of cheaply are old soviet parts. You can usually get 10 or more units for 1 of the old british parts.

<img class="padded center"
		alt="MP38A transistor"
		src="/images/2019-03-06-MP38A-transistor-pinout/IMG_8014.jpg"
	  srcset="/images/2019-03-06-MP38A-transistor-pinout/IMG_8014.jpg 1x, /images/2019-03-06-MP38A-transistor-pinout/IMG_8014-2x.jpg 2x" />

The part in question today is the Russian MP38A NPN Germanium Transistor. Ignoring the issue of reliablity and gain matching for a moment [^mp38aag1], just figuring out the pin outs are an issue when the datasheet is in Russian!

<!-- more -->

Whilst the layout is reasonably obvious I wasn't ever 100% sure.  Only once I built a [test circuit][tbetc] and it didn't work did I go googling again.

I found a page ([Blackout Electronics][be]) that posted a diagram which confirmed I was right which pin was the Base pin it wasnt clear which way the digram was showing the pins from.

So after getting it wrong once, then swapping it round my test rig started giving readings that made sense. They where rubbish, but made sense.

Rather than another diagram, here's an annotated photo which should be fairly unambiguous.

<img class="padded center"
		alt="MP38A transistor pin out"
		src="/images/2019-03-06-MP38A-transistor-pinout/IMG_8012-Edit.jpg"
	  srcset="/images/2019-03-06-MP38A-transistor-pinout/IMG_8012-Edit.jpg 1x, /images/2019-03-06-MP38A-transistor-pinout/IMG_8012-Edit-2x.jpg 2x" />

[^mp38aag1]: As the British parts are rarer, and more valuable they tend to come tested and known working.  For the old soviet parts you just buy a bag of 5/10/50 and you get what you get and have to test and rate them your self.

[tbetc]: http://tagboardeffects.blogspot.com/2012/08/germanium-transistor-tester.html
[be]: http://blackoutelectronics.com/wordpress/?p=445