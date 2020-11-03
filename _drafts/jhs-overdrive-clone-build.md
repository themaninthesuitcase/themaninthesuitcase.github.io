---
title: "JHS Overdrive Clone Build"
description: "A officially sanctioned act of pedal piracy"
categories:
 - guitar
tags:
 - diy
 - build
 - pedal
 - electronics
image: 
---

On Friday 2nd October 2020 [JHS launched their brand new 3 Series Pedal][jhs-3-series] line.  On the 7th October Josh, and the team, did a [live stream for Sweetwater][sweetwater-demo] where they demoed these.  During that stream Josh showed the schematics for all 7 of these new pedals and said the following:

<div class="text-center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/4jtfHNw4GRo?start=390" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<blockquote class="blockquote text-center">
    <p class="mb-0">
        Here's the schematic to this pedal. You can screenshot it, make it your self. We do not care.
    </p>
    <footer class="blockquote-footer">Josh Scott (2020)</footer>
</blockquote>

So screen shot it I did, and so began my journey cloning a brand new pedal.

<!-- more -->

## Schematic

The first job was to copy the schematic out from an iPad screen shot into something I can use.  I used [KiCad] for this project as it's open source (so free), reasonably well documented and fairly easy to use.  This is the same software I used for my [Katana 50 controller build][katana-50-post].

This wasn't too hard to do, the screen shot was pretty clear and so it was just a case of copying what I saw. A quick trip into Photoshop and some un-sharp mask helped reading a capacitor value and cropped off the black borders.  

<img class="padded center"
        alt="The original schematic shared by Josh"
        src="/images/jhs-overdrive-clone-build/JHS_Overdrive.jpg"
        srcset="/images/jhs-overdrive-clone-build/JHS_Overdrive.jpg 1x, /images/jhs-overdrive-clone-build/JHS_Overdrive-2x.jpg 2x" />

The diagram Josh showed didn't have any power section however.  As such I designed my own based on some previous experience and a [Brian Wampler][wamplerpedals] book I have which suggested 2 power filter caps, I was only going to add the single 47uF.  The design also called for 4.5V in some places.  I did this with a simple potential divider circuit.  I wasn't sure on what values to use for this but some quick research seemed to show that 10K was fine so I went with that.  A [Klon uses 27K][electrosmashklon], so I think I am probably in the right ball park here.

<img class="padded center"
        alt="The re-drawn schematic"
        src="/images/jhs-overdrive-clone-build/OverdriveSchematic.png" />

## PCB Design

This bit is a lot harder.  For this build I decided to try use some surface mount parts for the first time and get these assembled at the manufacturer.  What was to be SMD and what I would add later was decided on a part by part basis.

Almost all caps are to be soldered on as I chose to get name brand (Wima poly and Panasonic electrolytic) parts from RS Components, 2 tiny caps are SMD mainly as I was finding them hard to source.  C5/C6 are "extended" parts which means a £3 charge each to load less common parts them the machine. This sounds expensive but a Mica 51pF for C6 is £1.42 each and I'd need to order 50.  Or pay the £3 and they cost £0.0092 each after that.

Resistors are all SMD to save space and build time. I wouldn't expect them to affect the sound adversely as they are commonly used in modern production pedals, including those made by JHS. The hardest part was figuring out what wattage to go for.  Handily JHS quote a 12mA draw on the pedal giving 0.108W @ 9V. So a 1/8W should be fine as no single resistor has a full draw through it but leaves some headroom incase I am wrong.

All the diodes are SMD, mainly for size reasons but it also saves some build time and are a little cheaper that way.

The 2 transistors are only available as SMD, though I am sure I could have found a suitable through hole part if I'd wanted. These are also extended parts but I'd need to buy 100 (£3.30) from RS so the cost difference is pretty minimal and saves trying to hand solder SMD parts.

Finally I went for named Alpha 9mm pots and an RS pro switch to avoid nasty stuff from eBay and also mean I should be able to depend on them in future if I like them.

<img class="padded center"
        alt="Parts arriving for the build"
        src="/images/jhs-overdrive-clone-build/IMG_3598.jpg"
        srcset="/images/jhs-overdrive-clone-build/IMG_3598.jpg 1x, /images/jhs-overdrive-clone-build/IMG_3598-2x.jpg 2x" />

With all my parts chosen the software just dumps them into a mess on a new pcb, it's completely unusable like this.  My wife spent at least 30 minuted just dragging stuff apart so it was a bit more clear what we had to work with.

<img class="padded center"
        alt="Starting to sort the mess"
        src="/images/jhs-overdrive-clone-build/IMG_3568.jpg"
        srcset="/images/jhs-overdrive-clone-build/IMG_3568.jpg 1x, /images/jhs-overdrive-clone-build/IMG_3568-2x.jpg 2x" />

First job was to position the pots and switches as these are pretty limited to where they can go.  I used an old 1590B knock off I had to get some measurements and drew it up in [Inkscape] with the 3 knobs and the switch.  It was quite obvious the knobs would need to be no bigger than about 18mm or they just wouldn't fit or be usable.  After a bit of tweaking I was happy a 19.5mm spacing for the pots and positioned them on the PCB.  

<img class="padded center"
        alt="Testing the spacing for the pots using Inkscape"
        src="/images/jhs-overdrive-clone-build/Layout.png"
        srcset="/images/jhs-overdrive-clone-build/Layout.png 1x, /images/jhs-overdrive-clone-build/JHS_Overdrive-2x.jpg 2x" />

To add the switch I needed to first create a footprint for it.  Whilst RS provide one it's not compatible with KiCad, so I used the data sheet and created my own.  This isn't too hard and is quite quick to do. With this done I just dropped it in centred on the gain pot and as close as seemed sensible for a nice look.  I also positioned the input, output and power connections for the switch at the bottom to match the daughter board I had previously bought from [fuzz dog][fuzzdogdaughterboard].

The actual layout was just a case of putting things where they might make sense, then trying to wire stuff up.  If it didn't work I'd clearly all the wires move some bits and try again.  As things began to firm up I would lock them[^jhsod1] in place which stops you moving them by accident, and also means you they aren't cleared by default when you delete all.  Slowly but surely you end up with most things connected and after a final push with some vias I was able to connect everything.

I am pretty sure that if the fine people at JHS saw my routing they would be horrified. I found the SMD parts made things harder as all the SMD parts need to be on the same face (a limit from the manufacturer). As there are no through holes I couldn't just run lines one which ever side made more sense, but I got there in the end with some vias.  

I did try keep to some general rules I am aware of, don't run stuff parallel if possible, the 9V and 4v5 lines do for a while but I think this will be okay, make wires cross at 90° and generally try not to shove too much into a small area.  I also added a large ground plane to the bottom side which I hope will help with noise reduction.

<img class="padded center"
        alt="Final PCB design"
        src="/images/jhs-overdrive-clone-build/Overdrive_board.png" />

## PCB Manufacture

I went with [JLCPCB] again to get the PCBs, but have added a few options.  I am going for lead free boards and also removing their order tracking number.  Sadly as I am going for SMD assembly I can only select a green board, not black like I wanted.

Getting the boards made is just a case of following their guides on the web site.  They have guides specifically for KiKad for both [the boards][jlcpcb-gerber] and [assembly][jlcpcb-assem] stages.

There are a few extra steps needed for assembly that I didn't need for just ordering blank boards.  First you need to export a BOM, a positions file, and also you need to add some small holes[^jhsod2] to the board for location during assembly.  This is all documented in the help and is quite easy to do, if a little time consuming.

Manufacturing was a fair bit slower than my previous order.  I clearly hit a busy patch.

## A Problem
Before I get into the "how it was made" and "does it work" bit a brief note that shows I don't really know what I am doing and you shouldn't really be listening to me. I was reading a pedal breakdown, and noticed a 47uF capacitor from the 4.5V to ground in the power supply.  I don't have one.  I checked a few pedals: Boss DS-1, Ibanez Tubscreamer, Klon Centaur.  All of them have this 47uF cap in the 4.5v supply.

<img class="padded center"
        alt="Updated 1.1 Power section with C12 decoupling capacitor for the 4v5 supply."
        src="/images/jhs-overdrive-clone-build/PowerSection1_1.png" />

Apparently this is a [decoupling capacitor][wiki_decouplingcap] which is there to deal with voltage spikes or dropouts and also reduces the impedance (which is sort of like resistance but for AC and I am struggling to understand).  Clearly this is something that I should have added as it's a common feature, but alas, the boards were made before I noticed, but before they arrived.  Looking at the boards I am able to add in a capacitor from pin 1 of the volume pot to the closest ground pin.  Obviously this isn't ideal but it's also something I've seen in real products where something was missed out in early revisions.

## Assembly

First job is drilling out the enclosure.  Masking tape is applied to protect it and then careful measurements are needed to get everything in the right spot. Easier said than done, and things are a bit tight.  I did some tests on an old scrap enclosure to help check things and then made a few minor adjustments for the ones I will be using.  I wasn't sure on what jack I would be using due to space so this scrap test was useful in trying to get things to fit.

<img class="padded center"
        alt="Enclosure marked up for drilling"
        src="/images/jhs-overdrive-clone-build/IMG_3785.jpg"
        srcset="/images/jhs-overdrive-clone-build/IMG_3785.jpg 1x, /images/jhs-overdrive-clone-build/IMG_3785-2x.jpg 2x" />

With everything marked out I carefully centre punch each hole.  First is a 2mm drill, then a 4mm drill.  Finally a step drill is used to get each hole to final size.  These range from 7-12mm.  These are painted before final assembly.

{painted empty enclosure}

I normally use 60/40 leaded solder as I find it easier to solder with. For this project I am using lead free, I have some from previous projects, one is a standard type the other has some silver in it.  The goal being these are ROHS compliant, not that I need to worry about this as a hobbyist.  I went with some by [Rapid Electronics][RapidElectSolder], with my iron set to 350ºC this worked better than any other lead free I've used and was actually similar to the leaded solder I have.

<img class="padded center"
        alt="PCB as they arrived from manufacturing"
        src="/images/jhs-overdrive-clone-build/IMG_3778.jpg"
        srcset="/images/jhs-overdrive-clone-build/IMG_3778.jpg 1x, /images/jhs-overdrive-clone-build/IMG_3778-2x.jpg 2x" />

First I soldered the daughter boards to the foot switches and tested them with a multi meter for continuity. Essentially check the jack in goes to jack out, then click the switch and jack in should go to circuit in and circuit out to jack out.

{jack assembly}

The I added all the film capacitors first, followed by the electrolytics taking care of the polarity.  As I need to add on the missing coupling capacitor later I left the ground leg on C2 to help attach it later.  After the capacitors were on I added the socket for the op-amp.  As the legs are very short this is a bit fiddly but bending each corner holds it well enough to solder without too much movement.

The switch came next.  The legs on this are not going to bend to help hold it while soldering.  By luck the holes I designed were snug enough to hold it if I set the board vertical in the holder to do the first pin, before turning it over to finish the rest.

Last up, the pots.  The side support pins were problematic and didn't fit through the holes. A minor nudge with some pliers was needed to bring them in a little before they would fit.  On one I slightly over adjusted the legs.  On this one I applied solder to one support, then whilst holding the iron in place pushed the pot into place before removing the iron while still holding it.  This held the pot nicely allowing me to solder it in with out it moving.

<img class="padded center"
        alt="Initial board build up"
        src="/images/jhs-overdrive-clone-build/IMG_3779.jpg"
        srcset="/images/jhs-overdrive-clone-build/IMG_3779.jpg 1x, /images/jhs-overdrive-clone-build/IMG_3779-2x.jpg 2x" />

{adding the missing cap}

For the second board, rinse and repeat.

## Testing

## Lessons learnt

During this project I've learnt a few things and there are a number of things I would do differently.

First is I didn't research my power section enough.  Reading through some pedal breakdowns after I ordered the PCBs I quickly noticed the issue and so I should have looked at some other pedals for examples rather than using the basic one if the Wampler book.  This would have saved some stress and some awkward soldering.

The next one was I didn't think enough about the specs of the components I chose.  The electrolytic caps are all over spec'd for voltage significantly.  One is rated for 250V when 25V would have been enough, by going for a more reasonable spec these might have been physically smaller and so left more room on the board.  Well if they are available, parts availability seems spotty at the moment.

The toggle switch also falls into this area, I opted for a micro toggle switch.  I later discovered sub-micro switches which would have been a smaller footprint and often have stubby toggles which would have been a better fit for this use case.  Though these often don't use a securing nut which I am using to hide my sins from the drilling.

I also didn't take enough care about fitting in the footswitch and the jacks.  Whilst I was careful about space for the power jack I just didn't apply the same care for the rest.  This lead to issues getting my primary choices into the enclosure.  In future I would spend the time to make out the whole inside of the enclosure when designing the PCB, perhaps going as far as to design my own daughter board and PCB mounting both the foot switch and jacks more like a production pedal.

## Cost Breakdown

| Item                | Cost | Qty | Total |
|---------------------|-----:|----:|------:|
| Hammond 1590B       | 8.84 | 1   | 8.84  |
| RS Pro SPDT         | 1.85 | 1   | 1.85  |
| 3PDT                | 2.25 | 1   | 2.25  |
| 3PDT Daughter Board | 1.20 | 1   | 1.20  |
| LED                 | 0.54 | 1   | 0.54  |
| LED Surround        | 0.38 | 1   | 0.38  |
| PCB                 | 4.04 | 1   | 4.04  |
| TL072               | 0.78 | 1   | 0.78  |
| DIP-8 Mount         | 0.20 | 1   | 0.20  |
| DC Jack             | 0.59 | 1   | 0.59  |
| Neutrik Mono Jack   | 3.13 | 2   | 6.26  |
| Panasonic 47uF      | 0.38 | 2   | 0.76  |
| Panasonic 10uF      | 0.29 | 1   | 0.29  |
| Panasonic 1uF       | 0.30 | 2   | 0.60  |
| Wima 100nF          | 0.48 | 4   | 1.91  |
| Wima 220nF          | 0.73 | 1   | 0.73  |
| Alpha 9mm A500K     | 1.70 | 1   | 1.70  |
| Alpha 9mm B100K     | 1.70 | 1   | 1.70  |
| Alpha 9mm B25K      | 1.70 | 1   | 1.70  |
| Knobs               | 0.84 | 3   | 2.52  |
| __Total__           |      |     | __38.84__ |

_* Prices are inclusive of UK VAT @ 20%. Items sourced from various suppliers.  Prices do not include postage costs (around £10-15 so far) or additional items where there was a minimum order quantity. I did have a coupon for $8 off the SMD assembly which is not shown either._

_As such these costs are a guide. I ordered **at least** enough components for 2 complete builds, I am only missing the jacks and enclosures for 3 more so my costs where higher.  Please remember this was an exercise in learning not getting a cheap JHS pedal._

## Worth it?
Well, actual cash money? 1 pedal is quite a lot cheaper.  But I made 2 and have a bunch of stuff left over so less financially worth it than you think.

<img class="padded center"
        alt="I'm never gonna financially recover from this"
        src="/images/jhs-overdrive-clone-build/financially_recover.jpg" />

What's not factored in here is my time.  I spent between 3 and 4 hours copying the schematic and the checking it.  I don't know how long I spent on the PCB layout but it was 2-3 evenings so call it 8 hours, but almost certainly more.  I am also not counting the time spent looking at data sheets or looking up help docs on what I needed to get the boards fabbed or all kinds of time I spent on this.

Also not included is equipment. I have a soldering iron, PCB holders, drill, drill bits, measuring equipment etc.  If you don't you're going to need to buy them, I got some extra equipment to make this build easier.  And that adds up quite quickly I can assure you.

In all this was a lot of work to do.

This is where it gets awkward.  I don't know how much of the $/£99 JHS get but they £0.00 on this one.  That's no contribution to wages, equipment, facilities, R&D, Josh's pedal collection.  Nothing.  Whilst I can't see me making a pair of these causing them to go out of business if everyone did, they would and we'd all be poorer for it.  

Normally for my projects I throw them up on github or something so others can use them.  I am not doing that with this.  I would feel like I am making it too easy for you.  If you want to make a "cheap" Overdrive, the above tells you how I did it.  Now you go do it. If you don't want to work for it then please buy one from [Andertons][andertons-jhs-overdrive] \| [Sweetwater][sweetwater-jhs-overdrive] \| [Amazon][amazon-jhs-overdrive].  The first two aren't affiliate links, that Amazon one is. Choose wisely.

JHS did the actual work on these, so please pay them for it.

Thanks Josh for the schematic and the permission to build one.  This was a fun project and a welcome distraction from this year.

[^jhsod1]: Select the item them press L.  You can multi-select items with shift which makes locking in traces and blocks of components easier.
[^jhsod2]: I must have got this wrong as JLCPCB added more pre-manufacture.

[jhs-3-series]: https://www.jhspedals.info/3-series
[kicad]: http://kicad-pcb.org/
[katana-50-post]: /2019/09/18/katana-50-footswitch/
[sweetwater-demo]: https://youtu.be/4jtfHNw4GRo
[wamplerpedals]: https://www.wamplerpedals.com/
[electrosmashklon]: https://www.electrosmash.com/klon-centaur-analysis#power_supply
[inkscape]: https://inkscape.org/
[fuzzdogdaughterboard]: https://shop.pedalparts.co.uk/3PDT_True_Bypass_Daughterboard/p847124_12774515.aspx
[jlcpcb]: https://jlcpcb.com/
[jlcpcb-gerber]: https://support.jlcpcb.com/article/44-how-to-export-kicad-pcb-to-gerber-files
[jlcpcb-assem]: https://support.jlcpcb.com/category/78-smt-assembly
[andertons-jhs-overdrive]: https://www.andertons.co.uk/jhs-3-series-overdrive-pedal
[sweetwater-jhs-overdrive]: https://www.sweetwater.com/store/detail/JHS3OD--jhs-3-series-overdrive-pedal
[amazon-jhs-overdrive]: https://amzn.to/3128Wv8
[wiki_decouplingcap]: https://en.wikipedia.org/wiki/Decoupling_capacitor
[RapidElectSolder]: https://www.rapidonline.com/rapid-lead-free-solder-wire-22swg-0-7mm-100g-reel-85-1166

<img class="padded center"
        alt=""
        src="/"
        srcset="/ 1x, / 2x" />