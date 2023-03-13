---
title: 1590BB Enclosure for Tone Geek Aqua-Puss mk1 AP2 
description: 
categories:
- guitar
tags:
- diy
- pedal
- electronics
- wayhuge
- aquapuss
- delay
image: /images/2023-03-00-aqua-puss-clone-enclosure/CJP20210703-21039-2x.jpeg
---

I was lucky enough to get one of the first batch of PCBs for a [Tone Geek mk1 AP2 Aqua Puss][ttgap2].  This is a faithful replica of the 2nd version of the infamous Way Huge Aqua Puss, the mk1 AP-2.  There is an earlier AP-1 but thats true rocking horse poo. If you're reading this you probably know what this is.

The PCB is designed to fit the Mk2 enclosure, reasonably common despite being discontinued for the mk3 "smalls". Problem is I don't have one, and spending ~£100 for a used one just for the enclosure seems wasteful.

Whilst working on a Klone I made a discovery, it would fit inside a 1590BB. **Just**.

<img class="padded center"
    alt="AP2 PCB inside of a test 1590BB enclosure"
    src="/images/2023-03-00-aqua-puss-clone-enclosure/IMG_4913.jpeg"
    srcset="
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_4913.jpeg 1x,
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_4913-2x.jpeg 2x" />

After a lot of trial and error, involving cad models, 3D printed tests and 1 wrong metal enclosure I got it to fit.  **Just**.

<!-- more -->

Whilst it can fit it needs to be built to do so.  

Do not use the PCB insulator boards, they add height you don't have. I used vinyl cut on a plotter but it's not hard to hand cut. Mount the pots as close to the PCB as you can. I spaced them with a business card to stop them pushing directly and cutting the vinyl.

<img class="padded center"
    alt="Pots with vinyl applied for insulation"
    src="/images/2023-03-00-aqua-puss-clone-enclosure/IMG_5424.jpeg"
    srcset="
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_5424.jpeg 1x,
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_5424-2x.jpeg 2x" />

Make sure the big electro caps are firmly seated as these are the high points and there's not much clearance.

You will also need to use [Lumburg KLBM 3 Mono jacks][taydalumburg]. I find these to be the most compact available and are what are used in my build. Availability has been spotty on these over the last year or so but they can still be found.  RS do a very similar jack but the quality isn't as good.

<img class="padded center"
    alt="Inserted jack only just clears the PCB"
    src="/images/2023-03-00-aqua-puss-clone-enclosure/IMG_1779.jpeg"
    srcset="
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_1779.jpeg 1x,
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_1779-2x.jpeg 2x" />

On my most recent build I discovered a small change had been made to the Tayda enclosure lids. The older one had 2 small notches in the lid around 0.6mm deep. These gave the perfect amount of clearance when doing the final tests for the 2nd run. It's possible to address this with a small file to manually add the notch back in. Being so small and shallow this doesn't take long. The Tayda drill project has since been adjusted by 0.5mm which should be enough to resolve this with out going too far and hitting the PCB.

<img class="padded center"
    alt="Factory notched lid next to a manually notched one"
    src="/images/2023-03-00-aqua-puss-clone-enclosure/IMG_1406.jpeg"
    srcset="
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_1406.jpeg 1x,
        /images/2023-03-00-aqua-puss-clone-enclosure/IMG_1406-2x.jpeg 2x" />

If you'd like one for your build, you can order it from Tayda. Who can produce a completed enclosure ready for use.

<img class="padded center"
    alt="Completed AP-2 Pedal"
    src="/images/2023-03-00-aqua-puss-clone-enclosure/CJP20210703-21039.jpeg"
    srcset="
        /images/2023-03-00-aqua-puss-clone-enclosure/CJP20210703-21039.jpeg 1x,
        /images/2023-03-00-aqua-puss-clone-enclosure/CJP20210703-21039-2x.jpeg 2x" />

The knobs used are generic "klon style" black knobs for the main 2, with a Davies Moulding 1400 in the middle. This is a better match to the bigger knobs than the generic options. The [Davies Moulding 1470AQ](https://www.mouser.co.uk/ProductDetail/5164-1470AQ) for the main knobs, and [1400](https://www.mouser.co.uk/ProductDetail/5164-1400) are available from Mouser when in stock.

## Order your own enclosure

_**Disclaimer**_

*You use this at your own risk. Whilst I have ordered and used one with the below specifications I cannot guarantee it fits your build.  There was a minor tweak added after my most recent build to address the jack clearance issue detailed above.  This has not been tested but should fit.*

The enclosures are supplied by [Tayda](https://www.taydaelectronics.com), an electronics parts supplier based in Thailand. Ordering them is a multi-step process but not too complicated.

You will need to pick a 1590BB of your choice, I went with the [gloss white][taydaglosswhite] but [matt white][taydamattwhite] might work well too. You will also need to purchase the [custom drilling][taydadrilling], and if you want the design printed you need [UV Printing][taydauv], and [gloss varnish][taydagloss]. You need to order all 4 items: enclosure, drilling, UV printing and gloss varnish for this to work.

Once you have paid for your order of enclosure, drilling, UV and gloss you have to wait 15 minutes. In this time go to the drill layout link below and save it to your account. You also create a new UV template, with the below settings, upload the links PDF and save this as well.

<img class="padded center"
    alt="Tayda toolbox settings for UV printing"
    src="/images/2023-03-00-aqua-puss-clone-enclosure/Tayda UV Settings.png"
    srcset="
        /images/2023-03-00-aqua-puss-clone-enclosure/Tayda-UV-Settings.png 1x,
        /images/2023-03-00-aqua-puss-clone-enclosure/Tayda-UV-Settings-2x.png 2x"/>

After 15 minutes you will be able to create a drill job in the [Tayda toolbox](https://drill.taydakits.com/dashboard). Pick the drill layout and UV layout and submit it. In about a week or so a nice new enclosure will arrive at your door.

### Files

The drill layout is available here: [drill layout][taydaap2drill]

The PDF required for UV printing is here: [uv layout][ap2pdf] _(includes black design, and optional gloss layers)_

{% include donate.html %}

[ttgap2]: https://www.thetonegeek.com/single-post/aqua-puss-mk1-ap2-1998-style-pcb-now-available
[taydaap2drill]: https://drill.taydakits.com/box-designs/new?public_key=dEF3TzlhTFpGR1J2MFMxYlprLzFTQT09Cg==
[taydaglosswhite]: https://www.taydaelectronics.com/white-1590bb-style-aluminum-diecast-enclosure.html
[taydamattwhite]:https://www.taydaelectronics.com/matte-white-1590bb-style-aluminum-diecast-enclosure.html
[taydadrilling]: https://www.taydaelectronics.com/hardware/enclosures/enclosure-custom-drill-service/1590bb-custom-drill-enclosure-service.html
[taydauv]: https://www.taydaelectronics.com/hardware/enclosures/enclosure-uv-printing-service/1590bb-uv-printing-service.html
[taydagloss]: https://www.taydaelectronics.com/hardware/enclosures/enclosure-uv-printing-service/custom-uv-gloss-layer-service.html
[taydalumburg]: https://www.taydaelectronics.com/hardware/6-35mm-1-4-plugs-jacks/6-35mm-1-4-mono-phone-jack-socket.html
[ap2pdf]: /images/2023-03-00-aqua-puss-clone-enclosure/AquaPuss - BW - FOR TAYDA.pdf