---
title: Building 'The Kirkland Signature' Replica
description: "What do you do when you want something that you can't buy? #kirkboys"
categories:
 - guitar
tags:
 - build
 - pedal
 - electronics
image: /images/2021-12-01-building-the-kirkland-signature-replica/CJP20211122-21281.jpg
---

The Kirkland Signature was/is a pedal made by Josh Scott at [JHS Pedals][jhspedals] for John Mayer in 2017. It was used on his pedal board up until sometime in 2019[^kirksig1].

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-permalink="https://www.instagram.com/p/BR3kh3-D6Zm/?utm_source=ig_embed&amp;utm_campaign=loading" data-instgrm-version="14" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:540px; min-width:326px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:16px;"> <a href="https://www.instagram.com/p/BR3kh3-D6Zm/?utm_source=ig_embed&amp;utm_campaign=loading" style=" background:#FFFFFF; line-height:0; padding:0 0; text-align:center; text-decoration:none; width:100%;" target="_blank"> <div style=" display: flex; flex-direction: row; align-items: center;"> <div style="background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 40px; margin-right: 14px; width: 40px;"></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 100px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 60px;"></div></div></div><div style="padding: 19% 0;"></div> <div style="display:block; height:50px; margin:0 auto 12px; width:50px;"><svg width="50px" height="50px" viewBox="0 0 60 60" version="1.1" xmlns="https://www.w3.org/2000/svg" xmlns:xlink="https://www.w3.org/1999/xlink"><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(-511.000000, -20.000000)" fill="#000000"><g><path d="M556.869,30.41 C554.814,30.41 553.148,32.076 553.148,34.131 C553.148,36.186 554.814,37.852 556.869,37.852 C558.924,37.852 560.59,36.186 560.59,34.131 C560.59,32.076 558.924,30.41 556.869,30.41 M541,60.657 C535.114,60.657 530.342,55.887 530.342,50 C530.342,44.114 535.114,39.342 541,39.342 C546.887,39.342 551.658,44.114 551.658,50 C551.658,55.887 546.887,60.657 541,60.657 M541,33.886 C532.1,33.886 524.886,41.1 524.886,50 C524.886,58.899 532.1,66.113 541,66.113 C549.9,66.113 557.115,58.899 557.115,50 C557.115,41.1 549.9,33.886 541,33.886 M565.378,62.101 C565.244,65.022 564.756,66.606 564.346,67.663 C563.803,69.06 563.154,70.057 562.106,71.106 C561.058,72.155 560.06,72.803 558.662,73.347 C557.607,73.757 556.021,74.244 553.102,74.378 C549.944,74.521 548.997,74.552 541,74.552 C533.003,74.552 532.056,74.521 528.898,74.378 C525.979,74.244 524.393,73.757 523.338,73.347 C521.94,72.803 520.942,72.155 519.894,71.106 C518.846,70.057 518.197,69.06 517.654,67.663 C517.244,66.606 516.755,65.022 516.623,62.101 C516.479,58.943 516.448,57.996 516.448,50 C516.448,42.003 516.479,41.056 516.623,37.899 C516.755,34.978 517.244,33.391 517.654,32.338 C518.197,30.938 518.846,29.942 519.894,28.894 C520.942,27.846 521.94,27.196 523.338,26.654 C524.393,26.244 525.979,25.756 528.898,25.623 C532.057,25.479 533.004,25.448 541,25.448 C548.997,25.448 549.943,25.479 553.102,25.623 C556.021,25.756 557.607,26.244 558.662,26.654 C560.06,27.196 561.058,27.846 562.106,28.894 C563.154,29.942 563.803,30.938 564.346,32.338 C564.756,33.391 565.244,34.978 565.378,37.899 C565.522,41.056 565.552,42.003 565.552,50 C565.552,57.996 565.522,58.943 565.378,62.101 M570.82,37.631 C570.674,34.438 570.167,32.258 569.425,30.349 C568.659,28.377 567.633,26.702 565.965,25.035 C564.297,23.368 562.623,22.342 560.652,21.575 C558.743,20.834 556.562,20.326 553.369,20.18 C550.169,20.033 549.148,20 541,20 C532.853,20 531.831,20.033 528.631,20.18 C525.438,20.326 523.257,20.834 521.349,21.575 C519.376,22.342 517.703,23.368 516.035,25.035 C514.368,26.702 513.342,28.377 512.574,30.349 C511.834,32.258 511.326,34.438 511.181,37.631 C511.035,40.831 511,41.851 511,50 C511,58.147 511.035,59.17 511.181,62.369 C511.326,65.562 511.834,67.743 512.574,69.651 C513.342,71.625 514.368,73.296 516.035,74.965 C517.703,76.634 519.376,77.658 521.349,78.425 C523.257,79.167 525.438,79.673 528.631,79.82 C531.831,79.965 532.853,80.001 541,80.001 C549.148,80.001 550.169,79.965 553.369,79.82 C556.562,79.673 558.743,79.167 560.652,78.425 C562.623,77.658 564.297,76.634 565.965,74.965 C567.633,73.296 568.659,71.625 569.425,69.651 C570.167,67.743 570.674,65.562 570.82,62.369 C570.966,59.17 571,58.147 571,50 C571,41.851 570.966,40.831 570.82,37.631"></path></g></g></g></svg></div><div style="padding-top: 8px;"> <div style=" color:#3897f0; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:550; line-height:18px;">View this post on Instagram</div></div><div style="padding: 12.5% 0;"></div> <div style="display: flex; flex-direction: row; margin-bottom: 14px; align-items: center;"><div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(0px) translateY(7px);"></div> <div style="background-color: #F4F4F4; height: 12.5px; transform: rotate(-45deg) translateX(3px) translateY(1px); width: 12.5px; flex-grow: 0; margin-right: 14px; margin-left: 2px;"></div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(9px) translateY(-18px);"></div></div><div style="margin-left: 8px;"> <div style=" background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 20px; width: 20px;"></div> <div style=" width: 0; height: 0; border-top: 2px solid transparent; border-left: 6px solid #f4f4f4; border-bottom: 2px solid transparent; transform: translateX(16px) translateY(-4px) rotate(30deg)"></div></div><div style="margin-left: auto;"> <div style=" width: 0px; border-top: 8px solid #F4F4F4; border-right: 8px solid transparent; transform: translateY(16px);"></div> <div style=" background-color: #F4F4F4; flex-grow: 0; height: 12px; width: 16px; transform: translateY(-4px);"></div> <div style=" width: 0; height: 0; border-top: 8px solid #F4F4F4; border-left: 8px solid transparent; transform: translateY(-4px) translateX(8px);"></div></div></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center; margin-bottom: 24px;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 224px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 144px;"></div></div></a><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BR3kh3-D6Zm/?utm_source=ig_embed&amp;utm_campaign=loading" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">A post shared by John Mayer 💎 (@johnmayer)</a></p></div></blockquote> <script async src="//www.instagram.com/embed.js"></script>

Earlier this year I was looking for a new pedal/electronics project and for some reason this came to mind.

<!-- more -->

The info in Johns Instagram post is all that is known for certain. Josh isn't spilling the beans either other than to say "The circuit is really specific and that’s something that I’ve carefully kept private."

*Allegedly* [^kirksig2] based on the [JHS Prestige][prestige], no idea where that came from but I read it somewhere, but it sort of made sense so became the starting point. 

At this point a quick google usually gives you a schematic and a few dozen examples of other peoples builds. Not this time. Just a single thread on a forum, speculating and guessing based on a terrible quality photo.

After some research I learnt that the Prestige and Mini Bomb Boost used to share a PCB, with around half the components populated on each depending on what model was being built. This lead me to a [Japanese site][jprepair] documenting a Mini Bomb Boost needing a repair, which had some nice internal images.

Based on the speculation and tracing the circuit on the images I could tell the Prestige was similar to a [Soulsonic 'Crackle NOT Okay'][sscno]. As the images were for a Bomb Boost, I couldn't see what the actual values where but I could use the references to see if it was a resistor, capacitor, diode or transistor. In the end I went with a reasonably vanilla Crackle Not Okay, but added an extra resistor near the start to better match the Prestige. One day maybe I'll get hold of a Prestige and document the circuit and correct values.

The enclosure design is a best effort endeavour. It looked like a 125B size and shape so thats where I started. Using photoshop I was able to measure things and get a size for the knobs and positions for the LEDs and text. This is part guess work as there's only one image and it's not very square on. The font for the More/More-er took a bit of hunting to get a good match. The Kirkland logo made from the biggest logo I could find. The knobs had a very specific look I wanted to maintain vs some generic alternative. Thankfully I found exactly what was needed at [Thonk]. The end result isn't quite perfect but corrections would mean changes to not just the enclosure but the PCBs too. Also it's obsessing about tiny details no one cares about. 

<img class="padded center"
        alt="Comparison of the JHS and my pedal"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5736.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5736.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/IMG_5736-2x.jpg 2x" />

My first build was reasonably simple. 2 duplicate copies of the boost circuit and single large PCB mounting the footswitches, LEDs and points to wire in the jacks and DC socket. No batteries here. I of course messed up the first version, and had the input and output sides flipped. So v1.1 was ordered and worked as intended.

The 'Signature' on the enclosure was a bit more orange than expected from the colour in the design but in all I was happy.

<img class="padded center"
        alt="Complete V1 Kirkland Signature pedal"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5709.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5709.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/IMG_5709-2x.jpg 2x" />

When I posted a few photos online I got a surprising amount of requests to buy one. Initially I didn't plan to do much about this but after a while I decided I wanted to improve the design before I even considered it.

<img class="padded center"
        alt="Internals of the V1 pedal"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5711.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5711.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/IMG_5711-2x.jpg 2x" />

First job was to fix the enclosure. I made the red actually red. This alone made a huge difference. 

The second change you wouldn't see unless you took it apart. When adding the pots on the 1st pedal it was a pain to keep them in the correct orientation. I normally snap off the locating pin and rely on the fact there are multiple pots to hold the position. With just a single pot it was rotating more than I'd like. To fix this I added the extra hole in the enclosure for the locating pin on the pots which made assembling it much easier. 

The position of the ribbon cable mount was moved outwards to align better with the child circuits. I'd not used ribbon cable before and it wasn't very happy with the twist which made assembly tricky.

The last change was a super secret logo that shows it's one of mine, I can't imagine this will remain overly unique for long.

<img class="padded center"
        alt="New enclosure with pot location holes"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_6390.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_6390.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/IMG_6390-2x.jpg 2x" />

I also wanted to make the pedal **not** true bypass, this came from the comment in the instagram post *"Does it have true bypass circuitry? I really can't imagine that it does"*.

Based on the use on the tour board, dead last, it seemed an output buffer would be a nice addition to drive the cable back to the amp. Being no expert on buffers I went with the Klon buffer. I bread boarded one up and added it after the v1 pedal which worked great, so I updated the PCB with the design.  I opted for SMD for this as it kept it small and hidden under the board. There is also an added buffer bypass switch for those who aren't a fan of such things.

<img class="padded center"
        alt="Testing the new buffer circuit"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5799.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_5799.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/IMG_5799-2x.jpg 2x" />

Of course, I messed this up too and had the bias section wrong. So that was fixed and new boards ordered, again.

<img class="padded center"
        alt="Compared internals of the V1 and V2 pedals"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_6706.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_6706.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/IMG_6706-2x.jpg 2x" />

The final step was to build 5 of them. Being able to batch build was a new experience for me. I was able to pre prep all the components sat in front of the TV which made filling the panels of boards so much easier and faster. The slowest part was preparing all the wire and jacks. It's just a slow process to do by hand, well I used a drill to twist the wire. Each pedal has 6 wires with 2 ends that needs to be stripped, tinned and then soldered. Thats 36 operations per pedal, times 5 pedals.

<img class="padded center"
        alt="A pile of PCBs mid build"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_6645.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/IMG_6645.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/IMG_6645-2x.jpg 2x" />

The new enclosures looked far nicer with the rich red colour, and after a suggestion from my wife I also ordered 1 in Tesco Value[^kirksig3] colours to keep for my self, that is serial #1. This version came out really nice and worked well with the blue knobs and LEDs.

<img class="padded center"
        alt="Tesco Value branded pedal"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/CJP20211122-21277.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/CJP20211122-21277.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/CJP20211122-21277-2x.jpg 2x" />

What does it sound like? It's a boost. And then another  boost. They start as a buffer with a slight boost, slowly transitions to a mild boost at 12 o'clock and then dials in lots of gain from then onwards.

At the time of writing the first pedal (#2) is now sold, and #1 Tesco is mine, leaving 3 to go. I have boards for 4 more but I can't guarantee I'll make them all or that I won't order some more. What I can say is I have a new found respect for pedal companies. Building one is fun, building 5 is a task. I can't begin to imagine what building 50, 500, 5000 is like.

<img class="padded center"
        alt="Kirkland Signature Pedal"
        src="/images/2021-12-01-building-the-kirkland-signature-replica/CJP20211122-21281.jpg"
        srcset="/images/2021-12-01-building-the-kirkland-signature-replica/CJP20211122-21281.jpg 1x, /images/2021-12-01-building-the-kirkland-signature-replica/CJP20211122-21281-2x.jpg 2x" />

[^kirksig1]: Waits for Justin to correct him.
[^kirksig2]: Never believe anything you read on the internet.
[^kirksig3]: Tesco Value was a bit of a joke here in the early 2000s. It was Tesco's budget zero frills no effort brand. They did baked beans for 8p at one point. People started doing joke birthday cards and motivational posters so it got retired a few years ago. But the joke remains.

[jhspedals]: https://www.jhspedals.info
[prestige]: https://www.jhspedals.info/prestige
[sscno]: https://solgrind.wordpress.com/2009/01/08/crackle-not-okay/
[jprepair]: https://camuro-co-jp.translate.goog/blog/jhs-mini-bomb-boost-の修理＆モディファイ?_x_tr_sch=http&_x_tr_sl=ja&_x_tr_tl=en&_x_tr_hl=en-GB&_x_tr_pto=nui
[thonk]: https://www.thonk.co.uk
