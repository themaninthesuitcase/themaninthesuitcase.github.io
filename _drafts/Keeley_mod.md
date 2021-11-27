---
title: DIY Boss BD-2 Blues Driver "Keeley Mod"
description: How to ruin a perfectly fine "vintage" pedal.
categories:
- guitar
tags:
- diy
- pedal
- mod
- electronics
- boss
- keeley
---

One of the more famous pedal mods is the "Keeley Mod" that Robert Keeley used to do to the Boss BD-2. This modded pedal has been used by a number of great players including John Mayer which is how I've ended up here.

Being the person I am rather than buying a pre-modified pedal I decided to buy a standard pedal used and modify it my self.

If you want to do this your self then there is one gotcha. A year or so ago Boss changed from through hole to SMD components for the BD-2. Whilst this isn't impossible to mod it's a huge amount more work and not really worth it. So hit eBay and look for a used pedal. The ones you want have the power jack in the middle of the back like below, not the ones where the jack runs along the base plate.

{DC end plate photo}

Older pedals in blue boxes will be fine, the change happened during the current black boxes so you can't just go "black box is no good" as earlier once will still be mod-able.

Before we start: thanks to Ryan "[The Tone Geek][ttg]" who did most of this research and I am just following from his work and a few google searches.

<!-- more -->
## Table of Contents <!-- omit in toc -->

- [My BD-2 Pedal](#my-bd-2-pedal)
- [List of Changes](#list-of-changes)
- [Tools](#tools)
- [The Mod](#the-mod)
  - [Disassembling the pedal](#disassembling-the-pedal)
  - [Changing the components](#changing-the-components)
  - [Drilling the enclosure](#drilling-the-enclosure)
  - [Wiring the Phat capacitor](#wiring-the-phat-capacitor)

<blockquote class="blockquote text-right">
    <p><strong>Boss BD-2 Blues Driver Mods</strong></p>

    <p>This is not all-inclusive in what can be done to the Blues Driver. It is meant to give an idea of where the tone can be improved or changed. All of the changes are subtle but when packaged together offer a nice improvement.</p>

    <p>D3 Change this 1SS133 to a different (1N4002) diode for asymmetrical clipping. This adds second order harmonics. This adds to the tube type sound. I like the sound of this change.</p>

    <p>D7 D8 D9 and D10 Change 2 of of these diodes from 1SS133 to a single 1N4002. More second order harmonic distortion. Although the change is slight, I like it. We actually take out one of the two pairs and replace it with a single 1N4001.</p>

    <p>C1, C7, C6, C12, C13, and C15 Change this electrolytic capacitor to a 10uF Non-polarized caps. Non-polarized caps sound better . I like these anywhere there is signal coupling at this high a value.</p>

    <p>C14 Increase input coupling capacitor value to 0.1uF for increased bass response from your guitar.</p>

    <p>C100 Here is where we can affect the tone control. I prefer a little more lower-midrange and bass frequencies through the tone section. You can increase the lower frequencies by increasing the capacitor value to 0.033uF. Install a switch to add a 0.068uF cap in parallel with this value for the Phat Mode!</p>

    <p>Most of the ceramic caps are changed to Expensive Silver Mica (available through Small Bear Electronics www.smallbearelec.com or www.mouser.com or www.digiley.com). This is what makes our mod sound so good. A noticeable reduction in noise. An increase in the smoothness and no harshness left. This type of upgrade is not found in anyone's mods. The best sound is right here.</p>

    <footer class="blockquote-footer"><a href="https://web.archive.org/web/20080311111337/http://www.robertkeeley.com/product.php?id=14">Robert Keeley (2007)</a></footer>
</blockquote>

## My BD-2 Pedal

My personal pedal is from 1996, they launched in 1994 so it's reasonably early. I bought it "spares or repair" from a seller in Japan as it was the cheapest way to get one. Or so I thought! I had forgotten about the tax changes post Brexit so after those were added it ended up costing more or less the same as the ones for sale in the UK. So not a big saving as hoped but a story at least.

The only issue with the pedal found seems to be dirty jacks. Once cleaned with some [Servisol Super 10][amazonservisol] it has been behaving well. This is probably worth doing on any used pedal when it comes in just to help with reliability.

Other than that it has the typical old Boss pedal patina and the knobs are a little loser than ideal, but fine.

Being an old one I was hesitant to modify it but Boss must have made thousands of these each year so it's not exactly a rare piece and is hardly in museum condition.

## List of Changes

Over the time the mod has changed a little, my mod is based on a specific example but takes into account the research. In short there is not a single exact set of changes, but they are all reasonably close to each other. Note my mod isn't including the D3 change listed above as that wasn't in the pedal I have access to for reference.

| Reference            | Boss Value                  | Keeley Mod Value                  | Notes                                                                              |
|----------------------|-----------------------------|-----------------------------------|------------------------------------------------------------------------------------|
| C14                  | 0.047uf (47nf)              | 0.1uF (100nf)                     | Input capacitor lets more bass into the circuit                                    |
| C1 C6 C7 C12 C13 C15 | 10uf Polarized Electrolytic | 10uf Non Polarized Electrolytic   | Non-polarized caps sound better                                                    |
| C20 C25              | 100pf 10% ceramic           | 100pf 5% Silver Mica              | Lowers noise                                                                       |
| C21 C23              | 47pf 10%                    | 47pf 5% Silver Mica               | Lowers noise                                                                       |
| C26                  | 220pf 10%                   | 220pF 5% Silver Mica              | Lowers noise                                                                       |
| C100                 | 0.018uF (18nf) 10%          |                                   | Adds "a little more lower-midrange and bass frequencies through the tone section"  |
| -                    | -                           | 0.068uf (68nf) or 0.082uf (82nf)  | "Phat mod" the switch adds this in parallel to C100 for more bass \*               |
| D7 D8                | 1SS133                      | Single 1N4001                     | Adds second order harmonics                                                        |
| LED                  | Red                         | Ultra bright blue                 | Better visibility                                                                  |
| ~~D11~~              |                             | ~~11K~~                           | ~~Yes they really did replace a diode with a resistor! This is for the LED.~~ \*\* |

\* The phat mod, and some of the other changes seem to have evolved during the life of the "Keeley Mod". The phat mod capacitor has been both 68nf and 82nf, the larger the value the more bass you'll get so it's probably worth testing to see which you prefer.

\*\* I actually undid this mod and put the factory diode back. With the resistor in place the LED was always on dimly which the diode fixes. If you want the LED dimmer change R39 for something like a 3.9K or a 10K depending how much you want to dim it.

{schematic, small link to large}

(Click the image to open at full size)

I will be using quality branded parts for all of these changes. Cornell Dublier for the silver mica, Nichicon MUSE for the non polar[^bd2modmuse], Panasonic film caps On-Semiconductor didoes and Royal Ohm resistors. For the switch I have a Hongh branded switch, this is a company set up by an ex-Alpha engineer and I have found all of their parts to be very similar in quality and feel.

Whilst you could use other cheaper items, the list isn't very long and so you're not going to save a huge amount so may as well use the high end stuff if you can get it.

## Tools

On top of the replacement components you will need the following tools:

- A soldering iron, or soldering station.
- Solder, preferably leaded as it flows easier.
- Solder wick, to remove the old parts ([MG Chemicals][mgchemwick], [Hakko][hakkowick])
- (Optional) Solder pump (I like this [Engineer SS-02][engineerss02])
- Cutters to trim the components
- Wire strippers
- Small diameter heat shrink (1.5-2mm will be fine) around 5cm long.
- Small gauge wire around 0.25-0.35mm²/22-24awg, around 5cm long.

## The Mod

### Disassembling the pedal

For things like this I like to completely remove the circuit from the pedal. If you are skipping the phat mod this is probably unneeded but I dislike the idea of drilling into the enclosure with the important bits in the way. This probably isn't how Keeley did it as it's slower.

1. First remove the knobs, they should just pull off. Mine are a bit loose so came of easily but if they are proving tough use two small tea spoons to gently leaver them off.
1. Remove the back plate, and put this and the plastic shield to the side. Use a #2 [philips] screwdriver, not a [pozidrive] and do it by hand. They are actually [JIS] #2 but you almost certainly don't have one of those and a philips is a reasonable fit, just be gentle.
1. Put those 4 back plate screws into a cup, bowl, something that will stop them going missing. You won't be able to replace them like for like so losing them is going to suck.
1. Unscrew the nuts for the side jacks using a 12mm socket and put them in the cup with the washers. I like to use some [3D printed finger sockets][3dsockets] as they some me damaging things, but a normal socket works too just hold it in your fingers. Try avoid adjustable spanners, they have a habit of damaging things.
1. Unscrew the 3 nuts for the pots using an 11mm socket, into the cup with these and their washers.
1. Use a PH2 screw driver and remove a single screw holding the LED daughter board in place.

At this point you can remove the circuit from the case but it will still be held to it buy the battery and switch wiring.

To remove the remainder:

1. Push the switch up from inside the enclosure and out.
2. Carefully de-solder the 2 wires from the switch. The wires are just hooked over, once the solder is removed with a sucker a light tough with the iron will help it come away.
3. Push the battery clip through the hole.

### Changing the components

For each component follow the following:

1. Locate the component to replace on the circuit board.  Note C100 is on the board with 2 pots on it.
2. Now find the pads for that on the back of the board. Take your time here so you don't remove the wrong thing!
3. Apply a little new, preferably leaded, solder. This will heat the join a bit and adds fresh flux, helping the solder flow better for removal.
4. For bigger blobs I like to remove the bulk with a solder sucker. Heat the joint and quickly suck away the excess.
5. Re-tin your iron, go a little heavy, and using some solder wick apply the wick to the joint and then apply the iron. Watch the solder soak into the wick. Don't hold it too long or the pad may lift. Also take care to remove the wick and iron at the same time so that the wick doesn't stick to the pad and try to pull it off.
6. With the solder removed, if you're lucky, the part will fall out. If not heat the pads and gently wiggle the part until it comes out. Boss folded over the legs on most components so you may need to carefully bend the leg with the iron tip to free it. This isn't "good practice" but it's also the easiest way to do it in my experience.
7. Use some solder wick to clean the pad of excess solder.
8. Fit the replacement component. Take note of polarity of the diodes and LED and make sure you match it with the new parts. For the 1N4001 span both the old diodes (see image below if needed).
9. Resolder the new part and trim the leads. For capacitor C100 on the pot board do not trim the leads yet, we will do this later when we [add the phat cap][#Wiring-the-Phat-capacitor].

{Desoldered pads image}

{Updated board image}

### Drilling the enclosure

This is reasonably straight forward but I could have done a better job.

1. Put some masking tape on the face to the right of the word "Gain".
2. Mark a line along the center of the word Gain, I found this to be 7.5mm from the bottom edge.
3. Mark the point 5mm from the N in gain towards the edge.
4. Centre punch the cross.
5. Drill out with a small diameter drill bit as a pilot hole, I used a 1.8mm. This is where I went wrong as even with the punch it drifted about 1mm down.  Not a disaster but not the position I went for. A better center punch mark would probably have helped reduce this. Once a pilot hole is off you'll struggle to correct it.
6. Work your way up to a 6mm hole, I went 1.8mm, 2.5mm, 3mm, then swapped to a step bit for 4, 5, 6mm.

{marking}

Check that the switch fits in the hole. I chose to omit the external washer and set the nuts so that the out side one is mostly flush and hides the thread.

{finished switch mount}

### Wiring the Phat capacitor

1. Take the short length with and strip around 5mm off the end.
2. Twist the strands and lightly tin the end.
3. Bend a small hook about half way down, this will hook over the end of the leg of C100.
4. Hook over the wire as shown below and solder in place.  
5. Trim any excess wire.

6. Bend the legs of the capactor to form a straight wire.
7. Slide around 1cm of heat shrink onto each leg and bend in a hook as before with the wire.
8. Solder one end to the other leg of C100.
9. Trim the legs of C100, but leave a little spare in case you want to swap the phat cap in future so you have a bit more to work with.

<style>
  th, td {
    border-bottom: 1px solid #ddd;
    padding: 3px;
  }
  blockquote{
    font-size:unset !important;
    font-style: italic;
  }
</style>

[^bd2modmuse]: The pedal I have good photos of didn't use MUSE but another Nichicon range. However I have seen phots of Keeley modded pedals with the MUSE series capacitors. Also they are green.

[ttg]: https://www.thetonegeek.com/
[amazonservisol]: https://amzn.to/2XbVshu
[keeleybd2]: https://web.archive.org/web/20080311111337/http://www.robertkeeley.com/product.php?id=14
[philips]: https://en.wikipedia.org/wiki/List_of_screw_drives#Phillips
[pozidrive]: https://en.wikipedia.org/wiki/List_of_screw_drives#Pozidriv
[JIS]: https://en.wikipedia.org/wiki/List_of_screw_drives#JIS_B_1012
[engineerss02]: https://amzn.to/30Ty7Dt
[hakkowick]: https://amzn.to/3nXdbE3
[mgchemwick]: https://amzn.to/3E0ULYD