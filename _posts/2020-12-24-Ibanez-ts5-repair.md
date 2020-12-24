---
title: "Ibanez TS-5 Repair"
description: "Fixing a botched 808 mod"
categories:
 - guitar
tags:
 - diy
 - build
 - pedal
 - electronics
 - repair
image: /images/2020-12-24-Ibanez-ts5-repair/IMG_4088.jpg
---

The other week I bought a "spares or repair" Ibanez TS-5 Tube screamer from eBay for £25.  It was described as "intermittent" so I expected this to either be an iffy switch, similar to my [DL-5 delay][dl5], or maybe a broken solder joint to one of the jacks (including the power).

<img class="padded center"
        alt="My new TS-5 fresh out of the postage"
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4064.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4064.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4064-2x.jpg 2x" />

When the pedal arrived I gave it a thorough cleaning, as befitting our times though it also had 20+ years of grot on it.  There was a battery inside to that expired in 2011 and had burst.  Fortunately there was minimal damage to the battery clip.

<!-- more -->

Once inside the pedal it was very quickly obvious what the problem was: a badly done [808 mod][808mod]. The idea is by replacing the Op Amp with a JRC4558D and replacing a few resistors you end up with the same circuit as the vintage 808 Tubescreamer.  These were getting expensive at the time, but have now been re-issued.

<img class="padded center"
        alt="First look at the board"
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4070.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4070.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4070-2x.jpg 2x" />

So what was wrong? The IC was socketed, which was nice but they had done a terrible job removing to the old op-amp and adding the socket. The socket was only just about soldered on and 2 pads were almost completely missing once de-soldered.  This seemed like the primary cause of the "intermittent" issues.  They had also added an extra, what appeared to be germanium, diode in series with one of the clipping diodes.  I assume to add asymmetric clipping.  The final 2 changes where 2 resistors, R34 and R35 had been swapped to 808 specs, this was done much more cleanly.

<img class="padded center"
        alt="The original modder did a terrible job..."
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4071.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4071.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4071-2x.jpg 2x" />

My first job was to remove, and then replace the IC socket.  It seems they used leaded solder so this was reasonably painless.  With the part removed it was clear some significant damage had been done.  2 pads were at least half missing and 1 more was obviously beginning to lift.

<img class="padded center"
        alt="What's left of the solder pads"
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4078.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4078.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4078-2x.jpg 2x" />

To replace the socket I bent over the socket pins to mechanically hold the part in place.  On the damaged pads this also helped extend the pin into what remained of the pads.  One pad was so small I used the back of a scalpel to scrape away some of the solder mask.  This gave me a slightly larger area to solder to and help get a good connection.  The JRC4558D was put back as the original was now long gone.  I do have some TL072 but thats not what a Tubescreamer is about.

The diode was thankfully an easy fix.  They had kept the original and not clipped the leads.  Once the extra diode was removed I just needed to bend it back into place and then solder it.

<img class="padded center"
        alt="New IC socket and repaired clipping diode"
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4080.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4080.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4080-2x.jpg 2x" />

Finally the resistors were replaced with some 5% carbon film resistors of the original values.  The originals were smaller probably 0.25W where these are 0.5W so they look bigger but otherwise are the same thing.

<img class="padded center"
        alt="New resistors with the original values"
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4081.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4081.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4081-2x.jpg 2x" />

Whilst I was in there I also replaced the switch as I had some.  The pedal clearly has seen some use so it can't be far from dead now.

With it all back together all seems to be fine.  Before if you pressed the button repeatedly it would eventually stop the pedal working.  Now it doesn't do that.  

<img class="padded center"
        alt="The new soldering, a bit iffy but should hold"
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4083.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4083.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4083-2x.jpg 2x" />

So I now have my first tube screamer.  A bit worn and tatty but it works for my uses. Would I trust it to play a show, if I ever do? Maybe.  I don't stomp hard so the socket should be okay vs hard soldered.  It sounds like a Tubescreamer and works so feels like a win to me!

<img class="padded center"
        alt="The fully repaired TS-5"
        src="/images/2020-12-24-Ibanez-ts5-repair/IMG_4088.jpg"
        srcset="/images/2020-12-24-Ibanez-ts5-repair/IMG_4088.jpg 1x, /images/2020-12-24-Ibanez-ts5-repair/IMG_4088-2x.jpg 2x" />

[dl5]: /2020/07/12/ibanez-soundtank-dl5-repair/
[808mod]: http://www.planeteleven.net/tubescrmr/
