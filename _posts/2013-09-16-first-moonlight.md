---
title: "First Moonlight"
---
I have recently been starting to investigate the world of astronomy and astrophotography. After a lot of reading up on the subject on a clear I went out to photograph the moon seriously for the 1st time, "first light" being the astronomy slang for the 1st time you use something.

[caption id="attachment_1121" align="aligncenter" width="600"]<a href="http://www.cpearson.me.uk/wp-content/uploads/2013/09/2013-09-16-Moon.jpg"><img class="size-medium wp-image-1121" alt="A waxing gibbous moon (91%) imaged from Surrey, UK." src="http://www.cpearson.me.uk/wp-content/uploads/2013/09/2013-09-16-Moon-600x600.jpg" width="600" height="600" /></a> A waxing gibbous moon (91%) imaged from Surrey, UK.[/caption]

<!--more-->Taking the images with a modern DSLR and photographic lens isn't overly complex.  Focus using autofocus, set a good exposure (I used <a href="http://en.wikipedia.org/wiki/Exposing_to_the_right" target="_blank">ETTR</a> here to ensure nice noise free images) then fire.  The key difference to terrestrial images is volume of data.

Astophotography almost always makes use of stacking to take lots images to make 1 final image.  Using the self timer I took around 140 images with a 1 second interval, exposure was around 1/320 f8 ISO800 from memory.  This was long enough for the moon to move from centre frame to the edge on my 600mm focal length.

With the images in the can comes processing.  First step was to use lightroom to export the NEF images to the TIFF as the NEF files aren't supported by the software I was using. To do this I zero'd out all adjustments and exported as a full quality TIFF.

Next I used a tool called <a href="https://sites.google.com/site/astropipp/" target="_blank">PIPP</a>.  This is used to do several things, rates all the images by their quality so you can pick the best x%, finds the imaged object and auto crops to fill the frame and optionally convert to monochrome which I did here.  The moon does have a lot of colour but I had read for beginners it's easier to start in mono. This done I exported a set of the best 100, according to PIPP, pre-processed TIFFs for the next step.

The TIFFs where now loaded into a package called <a href="http://www.astronomie.be/registax/" target="_blank">Registax</a> to perform the stacking.  For the most part this was a simple "next next next" process but I did fiddle with some settings to see what they did. Once stacked you get to where the main magic happens, wavelets.  These use some form of maths witchcraft to pull vast amounts of detail from a blurry image.

The final image was then exported as a TIFF and imported back into Lightroom for a few final tweaks to the brightness and resizing for web.

Initial feedback on astro site stargazers lounge was positive but I did get some feed back for next time out. You can read the thread here: <a href="http://stargazerslounge.com/topic/195205-first-lunar-image/">http://stargazerslounge.com/topic/195205-first-lunar-image/</a>

For those using non Windows platforms all the above was done on a Macbook Pro running OSX 10.8, no Windows install was used.  PIPP and Registax are installed under <a href="http://www.winehq.org/" target="_blank">wine</a> which in turn I installed using <a href="http://brew.sh/" target="_blank">homebrew</a>.  Feel free to contact me for help here if you need it.
