---
title: Cloning the Vemuram TSV808 with The Tone Geek
description: Helping to turn Unobtainium into Obtainium.
categories:
- guitar
tags:
- diy
- pedal
- electronics
- vemuram
- ibanez
- tubescreamer
image: /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8962.jpeg
---

The Vemuram TSV808 is a sort of modified of a Tubescreamer/JanRay hybrid. It's also incredibly high end, initially selling for $499, if you could get one in the limited release, and are now being listed on the [used market for £1200-£1800 or more.][reverbtsv808]

The internet has allowed me the chance to get to "meet" and speak to people all over the world. One of those is Ryan [The Tone Geek][ttg]. We often talk guitars, pedals, electronics and what ever dumb stuff that comes up.

One evening Ryan sent me a photo of a Vemuram TSV808, a multimeter and a ton of hand drawn documentation. After a bit of conversation I suggested bread boarding it to check the schematic. "I find that so borinnnggggg" came the reply, and after a few more messages back and forth, I had my own copies of the board layout and first pass hand drawn schematic.

My first task was to turn the hand drawn document into a digital one that is easier to maintain and share. I use [KiCad] for this, which took me an evening. Something about this project had grabbed me and I just had to do it. Whilst creating this schematic I checked values against both the photos of the board I got from Ryan, but also some found on google.
As I was doing this my wife re-drew the board layout to be a bit more legible where some items had been squashed together.

<img class="padded center"
        alt="Starting to build the bread board"
        src="/images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8729.jpeg"
        srcset="
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8729.jpeg 1x, 
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8729-2x.jpeg 2x" />

<!-- more -->

With a schematic in place it was time to try bread boarding it. I printed the schematic to allow me to mark what was done, and with some pretty cheap parts I had in stock. Whilst I had most parts, some had to make do was as close as I had to hand. I always start with the power section as everything else will hang off it. Followed up with building up the first op amp stage (the gain and clipping circuit) on the bottom half of the board, then the tone stack and 2nd op amp stage (I think amplification and tone shaping) on top half.  I started this at 4pm and by 6pm I had a working, reasonably close clone of the TSV808, 3 days after first getting the documents. Not only that but it worked, and sounded great.

<img class="padded center"
        alt="Testing the first completed breadboard"
        src="/images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8734.jpeg"
        srcset="
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8734.jpeg 1x, 
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8734-2x.jpeg 2x" />

With the first prototype complete I ordered the parts I did not have to hand and fixed an issue where I had the Gain pot backwards. Due to the COVID parts shortages I couldn't get trim pots with thumb knobs and made do with some that need a screw driver.

The next step was to start building a BOM, or more accurately 2.

The first was an accurate one using as many accurate parts from the original as possible.  This was the start of the mouser BOM, I found the film caps, DALE CMF55 resistors and then picked out a set of Koa Spear resisters for the rest [^tsv8081]. Ryan managed to find the correct poly caps and some really nice polymer capacitors to replace the custom electrolytics used.

The 2nd BOM was a more "budget" Tayda bom, though the Mouser one isn't a huge amount more, and you'll need to order some bits from Tayda such as the enclosure anyway.  This swaps the majority of parts for more standard ones, though by no means rubbish, and I selected these to allow me to build a reasonably close version but $10 or so cheaper per pedal.  The major changes where standard electrolytic caps, the mica caps were swapped to ceramic, and the tone capacitors from rolled to dipped polyester film.  

Spoiler: Both BOMs basically sound the same ± pot tolerances.

At the start the OpAmp was still unknown, so the tried and true 4558D(D) was chosen. Mouser stock the 4558DD if you want some of the fancy ones. Later that was found to be the OPA2134.

Whilst all this was happening Ryan was doing his thing with the PCB layouts. This is the point where the 9mm trim pots were chosen, but for the most part this is where Ryan excels so he was always ahead to me! He's documented his side of all of this [on his site][ttgats808].

At this point we had all we needed to order PCBs. For reference this was less than a week from those first photos changing hands.

Before the order went in I did one last thing. I hate hand wiring foot switches as it's too fiddly, so created a small daughter board to match the layout Ryan did.

<img class="padded center"
        alt="Checking the layout of the daughter board"
        src="/images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/Daughter.jpeg"
        srcset="
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/Daughter.jpeg 1x, 
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/Daughter-2x.jpeg 2x" />

Pretty soon stuff started arriving and I was able to build up the first ATS808 using the Tayda BOM to prove it. It worked! but there was 1 small issue: the volume pot was backwards.  This was fed back to Ryan and fixed going forwards.  Fortunately this is an easy fix with some wire to "flip" the pot.

<img class="padded center"
        alt="The first completed ATS808 using the Tayda parts"
        src="/images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8962.jpeg"
        srcset="
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8962.jpeg 1x, 
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_8962-2x.jpeg 2x" />

I used this for a while before building a 2nd using the accurate parts into a hammered copper enclosure which looks fantastic. I still haven't gotten round to ordering the correct OPA2134 chip so I am currently using a 4558DD.

<span class="center">[REPLACE THIS IMAGE]</span>
<img class="padded center"
        alt=""
        src="/images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_0337.jpeg"
        srcset="
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_0337.jpeg 1x, 
            /images/2022-11-16-cloning-the-vemuram-tsv808-with-the-tone-geek/IMG_0337-2x.jpeg 2x" />

If you wish to buy your own ATS808, either as a kit or built, check out [The Tone Geek Shop][ttgshop] where you can purchase not just the ATS808, but also a number of other products that are all excellent. I have the VS10, mk1 AP2 as well as the Black Triangle (which I still need to build).


<img class="padded center"
        alt=""
        src="/"
        srcset="/ 1x, / 2x" />

[^tsv8081]: We're not sure what Vemuram used for the majority of resisters but they do look like Royal Ohm to me. These are affordable and available from [Tayda][taydaresistors].

[reverbtsv808]: https://reverb.com/uk/p/ibanez-tsv808-vemuram-tube-screamer#listings
[ttg]: https://www.thetonegeek.com
[ttgshop]: https://www.thetonegeek.com/shop
[ttgats808]: https://www.thetonegeek.com/single-post/above-top-secret-reverse-engineering-the-vemuram-tsv808
[kicad]: https://www.kicad.org
[taydaresistors]: https://www.taydaelectronics.com/resistors/1-4w-metal-film-resistors.html