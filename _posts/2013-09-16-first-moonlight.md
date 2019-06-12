---
title: "First Moonlight"
categories:
 - photography
tags:
 - astrophotography
 - moon
 - software
---
I have recently been starting to investigate the world of astronomy and astrophotography. After a lot of reading up on the subject on a clear I went out to photograph the moon seriously for the 1st time, "first light" being the astronomy slang for the 1st time you use something.

<img class="padded center"
		alt="A waxing gibbous moon (91%) imaged from Surrey, UK."
		src="/images/2013-09-16-first-moonlight/2013-09-16-Moon.jpg" />

Taking the images with a modern DSLR and photographic lens isn't overly complex.  Focus using autofocus, set a good exposure (I used [ETTR][ettr] here to ensure nice noise free images) then fire.  The key difference to terrestrial images is volume of data.

<!-- more -->

Astophotography almost always makes use of stacking to take lots images to make 1 final image.  Using the self timer I took around 140 images with a 1 second interval, exposure was around 1/320 f8 ISO800 from memory.  This was long enough for the moon to move from centre frame to the edge on my 600mm focal length.

With the images in the can comes processing.  First step was to use Lightroom to export the NEF images to the TIFF as the NEF files aren't supported by the software I was using. To do this I zero'd out all adjustments and exported as a full quality TIFF.

Next I used a tool called [PIPP][pipp].  This is used to do several things, rates all the images by their quality so you can pick the best x%, finds the imaged object and auto crops to fill the frame and optionally convert to monochrome which I did here.  The moon does have a lot of colour but I had read for beginners it's easier to start in mono. This done I exported a set of the best 100, according to PIPP, pre-processed TIFFs for the next step.

The TIFFs where now loaded into a package called [Registax][registax] to perform the stacking.  For the most part this was a simple "next next next" process but I did fiddle with some settings to see what they did. Once stacked you get to where the main magic happens, wavelets.  These use some form of maths witchcraft to pull vast amounts of detail from a blurry image.

The final image was then exported as a TIFF and imported back into Lightroom for a few final tweaks to the brightness and resizing for web.

Initial feedback on astro site stargazers lounge was positive but I did get some feed back for next time out. You can [read the thread here][sgl]. 

For those using non Windows platforms all the above was done on a Macbook Pro running OSX 10.8, no Windows install was used.  PIPP and Registax are installed under [wine][wine] which in turn I installed using [homebrew][brew].  Feel free to contact me for help here if you need it.

[ettr]: http://en.wikipedia.org/wiki/Exposing_to_the_right
[pipp]: https://sites.google.com/site/astropipp/
[registax]: http://www.astronomie.be/registax/
[sgl]: http://stargazerslounge.com/topic/195205-first-lunar-image/
[wine]: https://www.winehq.org
[brew]: https://brew.sh
