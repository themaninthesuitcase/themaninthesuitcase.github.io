---
title: "Adobe Lightroom 4 Beta Review"
catagories:
 - photography
tags:
 - review
 - software
 - adobe
 - postprocessing
---
January 10th 2012 saw Adobe release an open beta of Lightroom 4, 6 years after Lightroom 1 hit the shelves.  In this period the product has changed massively but what does this new version bring to the table.

Adobe have made a few changes to existing features and also add some new ones, including a new Map module.

As stated in the title, this is a beta, so there **will** be dragons.  To help keep support issues down Adobe don't let you convert old catalogues.  Instead they recommend you make copies of some files and then import and work on those, never work on the originals as they won't be there to pick up the pieces when it all goes wrong.

## Basic Panel and Rendering engine

<img class="padded center"
		alt="Lightroom 4 Beta Basic Panel"
    width="500px"
		src="/images/2012-01-11-adobe-lightroom-4-beta-review/Screen-shot-2012-01-11-at-21.38.46.png" />

Potentially one of the biggest changes is Adobe have updated the basic panel in the develop module.  They have removed brightness and renamed a few other sliders.  The result is a much simpler interface that I feel works well and is much more intuitive in use.

<img class="padded center"
		alt="Updated Process Engine Option"
    width="500px"
		src="/images/2012-01-11-adobe-lightroom-4-beta-review/Screen-shot-2012-01-11-at-21.41.43.png" />

Images edited using the old panel (still accessible using the old 2010 process method) will map their settings into the new panel so you won't loose edits when you update into the new 2012 processing engine.

The new 2012 rendering doesn't seem to have made any huge leaps forward as with the <abbr title="Lightroom 2">LR2</abbr> to <abbr title="Lightroom 3">LR3</abbr> change.  The Noise reduction seems unchanged and the general result seems to be identical when comparing to LR3, at least to my eyes.

The end result of these two changes to the panel and rendering engine are more of an evolutionary change.  The net result is similar, if not identical, only the route to it has changed a small amount.

## Softproofing

One of a few true new features in Lightroom 4 is soft proofing, previously only available via Photoshop this may prove to be a useful addition.

<img class="padded center"
		alt="The Soft Proof Screen"
    width="500px"
		src="/images/2012-01-11-adobe-lightroom-4-beta-review/Screen-shot-2012-01-11-at-21.46.46.png" />

Having never used it before I was unsure what soft proofing was and how it would help me, especially as I don't colour calibrate my monitors.  However after watching the [Adobe TV video][adobeSoftProof] on the subject I can see this being a useful feature for people who print a lot and are often disappointed with the results or have troubles with jpegs when exported for web viewing.

## Map Module

For me this is the biggest new feature in version 4.  Lightroom now supports GPS tagging and viewing on a map natively.  Previously Lightroom only displayed the GPS if it was already in the EXIF from the camera, though there was a [plugin][friedlGps] that allowed you to map in GPS position from a track.  This is now all handled natively within Lightroom 4.

<img class="padded center"
		alt="The Map Module"
    width="500px"
		src="/images/2012-01-11-adobe-lightroom-4-beta-review/Screen-shot-2012-01-11-at-21.48.35.png" />

If you have a camera with GPS you need do no more, your images will show on the maps and you're done.  If you don't there's a couple of ways to add this GPS data after the fact.

The first way is a simple drag and drop onto the map.  This is very similar to what Flickr uses and very simple.  Simply find the location (via search or manually) then drag the image(s) on to the map to add an exact GPS point to the image.  Done.

The other way, which is how the plugin works, is to use a GPS track log and then sync this against the photos.  The idea behind this is you use a GPS device to record a log of your position while taking photos then using the time stamps of the locations and the photos sync the two.  I am yet to try this as I don't have a GPS log and photo set but I will try it before the beta expires to see how it works.

Personally I like the idea of an external GPS unit as then I am not using camera battery maintaining a GPS lock, the UI is better (can see accuracy and position not just on/off) and I can use it for other tasks.

<img class="padded center"
		alt="Remove Location Option on Export"
    width="500px"
		src="/images/2012-01-11-adobe-lightroom-4-beta-review/Screen-shot-2012-01-11-at-21.54.06.png" />

The main concern I had with GPS tagging was that of privacy. While I might want to tag my shots of the kids were at home or where that rare bird was it doesn't mean I want to share this information with the world. Fortunately there's a single check box in the export wizard which will remove all location information from the exported image keeping this data private.

## Books

Another new feature is the ability to create photo books direct from Lightroom.  This is a feature provided by Apple in both iPhoto and Aperture. The books are provided by [Blurb][lr4blurb], I haven't used them my self but have heard good things.  Had this been in Lightroom before I would have considered them when I made a photo book.  Pricing isn't the cheapest but the quality is supposedly good and if the integration is any good this could be a winner.

It also looks like you can export PDF versions, but I haven't tried this only seen it in the menus.

## Video

Adobe seem to be making a big deal of the new video support.  Though from what I have seen this is primitive at best and you'd be far better off using iMovie or Windows Movie maker which can do all that Lightroom can and more.

## Conclusions

Based on the March 31st expiry date on the beta, we're looking at a spring launch of the final product.  Will I be swapping over to the new version?  Well it depends.

Currently Lightroom 3 retails for £240, this is more than 4 times what Apples Aperture 3 costs via the App store (or 2x the price from Apple on DVD).  Unless Adobe cut the price significantly I can't see me making the change to Lightroom 4, and would probably want to look at getting an Aperture trial working[^lr4fn1].  Other than the map feature, which is already in Aperture 3, there is no 1 killer feature I feel is worth the potential huge cost.

## *Update*

*Lightroom 4 was released earlier this week (March 6th, 2012), and they have halved the price!  Priced at about £105 (depending on delivery choice) for a full Win/Mac copy or about £60 for the upgrade or Student versions.  As I am eligible for education pricing £60 is certainly worth a purchase especially as it's now a Win/Mac copy not single platform as before.  All I need to do now is dig out the proof to send to Adobe.*

## Lightroom 4 Resources

 * Adobe Labs download page for Lightroom 4 - [Adobe Labs download page for Lightroom 4][adobeLr4]
 * Adobe TV video introduction series - [Adobe Announces Lightroom 4 Beta][adobelr4blog]

[^lr4fn1]: I squandered my free trial by not using it for the 30days allowed as many often do!

[adobeLr4]: http://labs.adobe.com/technologies/lightroom4/
[adobelr4blog]: http://blogs.adobe.com/jkost/2012/01/4267.html
[lr4blurb]: http://www.blurb.com/lightroom
[friedlGps]:http://regex.info/blog/lightroom-goodies/gps
[adobeSoftProof]: http://tv.adobe.com/watch/whats-new-in-lightroom-4-beta/soft-proofing-and-dng-enhancements/
