---
title: GIMP Star Trails
description: An update on my opensource GIMP plugin.
categories:
 - tech
tags:
 - mac
 - linux
 - opensource
 - oss
 - plugin
 - astro
 - astrophotography
---
Way back in 2011 I was bitten by the astrophotography bug and enjoyed taking star trail photography.  For those who aren't aware what that is, here is a brief summary from wikipedia:

> A star trail is a type of photograph that utilizes long-exposure times to capture the apparent motion of stars in the night sky due to the rotation of the Earth. A star trail photograph shows individual stars as streaks across the image, with longer exposures resulting in longer streaks. Typical exposure times for a star trail range from 15 minutes to several hours, requiring a 'bulb' setting on the camera to open the shutter for a longer period than is normal.
>
> <cite> &mdash; [Wikipedia (2016)][wiki]</cite>

At the time there was no free software for the mac so I wrote a plugin for the free image program [GIMP][gimp][^gimpst1].  This got a reasonable amount of use by others but not long after a few more fully featured software became available, I *ahem found ahem* Adobe Photoshop (and now pay for it) and the plugin fell by the way side.

<img class="padded center"
		alt="Star trail"
		src="/images/2016-08-18-gimp-startrail/CJP20110408-0801.jpg"
	  srcset="/images/2016-08-18-gimp-startrail/CJP20110408-0801.jpg 1x, /images/2016-08-18-gimp-startrail/CJP20110408-0801-x2.jpg 2x" />

Where am I going with this? Well being an open source project on github other users are able to contribute fixes and new features.  This week exactly [this happened][pr].  The new change adds a basic method to remove sky glow from the image as well as a few other minor bits.

The incredibly well named _gimp-startrail-compositor_ 1.8 is [available on github][gsc].

[wiki]: https://en.wikipedia.org/wiki/Star_trail
[gimp]: http://www.gimp.org/
[pr]: https://github.com/themaninthesuitcase/gimp-startrail-compositor/pull/2
[gsc]: https://github.com/themaninthesuitcase/gimp-startrail-compositor

[^gimpst1]: Yes that really is the name of the software.
