#Making GIFs with Photoshop

Making GIFs is currently becoming one of the most important things in my toolkit, mostly because they make tweets look better and furnish articles well. However, you need to be careful of both size and content in order to meet space requirements, as the file format is inherently large due to its age and poor optimization.

This can be worked around in certain stages, but sadly people haven't phased GIFs out entirely due to a couple reasons (by my thoughts, at least):

1. They auto-play on Twitter instead of requiring a user to click through. They also play on hover for other services (Tumblr, Facebook, etc)
2. They are accepted by many older services, especially ones that don't accept embedding your own HTML (like Pinterest)
3. GIFV, GFYs and .WebMs have yet to come up with a format that works for everyone and are accepted on all platforms

It sounds silly, but even putting one button for people to click (like playing a video or .WebM) might be enough for people *not* to click on it. Sadly, that's how content works sometimes.

#This guide requires:

* Photoshop
* Mild video editing

The reason we're using Photoshop instead of some kind of other editor or drag-and-drop GIF maker is because I like to know how big the output GIF is going to be, and have fine-tuning over different things like how fast it runs, what the colors look like, and its end dimensions. If you're in an absolute hurry, sure, you can use one of those services, but you're usually going to have to put up with bad compression, a watermark logo, or something that ultimately looks bad or doesn't fit your needs.

#Table of Contents

* [Step 1: Getting your video](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-1-getting-your-video)
* [Step 2: Importing into Photoshop](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-2-importing-into-photoshop)
* [Step 3: Dealing with what comes out](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-3-dealing-with-what-comes-out)
* [Step 3b: Resizing our image (optional)](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-3b-resizing-our-image-optional)
* [Step 4: Saving our GIF](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-4-saving-our-gif)
* &nbsp;&nbsp;&nbsp;&nbsp;[Optimizing our GIF - why settings matter](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#optimizing-our-gif---why-settings-matter)
* &nbsp;&nbsp;&nbsp;&nbsp;[Resizing our image - why reprocessing matters](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#resizing-our-image---why-reprocessing-matters)
* &nbsp;&nbsp;&nbsp;&nbsp;[Comparing changes using 2/4-Up](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#comparing-changes-using-24-up)
* &nbsp;&nbsp;&nbsp;&nbsp;[Custom settings - what they mean](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#custom-settings---what-they-mean)
* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Color reduction](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#color-reduction)
* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Dithering](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#dithering)
* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Web Snap and Lossy](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#web-snap-and-lossy)
* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Saving custom settings](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#saving-custom-settings)
* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Looping once vs forever](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#looping-once-vs-forever)
* [Step 5: Finishing up](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-5-finishing-up)
* [Other optional steps and tweaking before saving](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#other-optional-steps-and-tweaking-before-saving)
* &nbsp;&nbsp;&nbsp;&nbsp;[Removing frames](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#removing-frames)
* &nbsp;&nbsp;&nbsp;&nbsp;[Color correction and adding overlay text/images](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#color-correction-and-adding-overlay-textimages)
* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Ensuring consistency](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#ensuring-consistency)
* &nbsp;&nbsp;&nbsp;&nbsp;[Increasing pause between frames](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#increasing-pause-between-frames)
* [Wrapping it all up](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#wrapping-it-all-up)
* Licensing

#Step 1: Getting your video

I know I mention video, but that is what we make our GIFs out of. [You can download this video as a sample](https://www.dropbox.com/s/9j78myctwhwjss1/tozawa.mp4?dl=0) from my Dropbox.

Keep in mind that the size of the video matters; Photoshop can only import 500 frames of a video at maximum. When you import the video into Photoshop (in order to do the GIF work) it will tell you that it's either a large video in size and/or in frames. The large size of a video can make it difficult to work with, as changes will need to be applied to the whole thing.

For this tutorial I'll be using Photoshop CS6.

#Step 2: Importing into Photoshop

After opening Photoshop, we can import our video by going to **File > Import > Video Frames to Layers**.

![Photoshop step 1 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop1.jpg?raw=true)

After a bar fills up, you'll get this window, which allows you to choose what you'll be importing out of the video.

![Photoshop step 2 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop2.jpg?raw=true)

As you'll notice, you have some options here. 

**Range to Import** is self-explanatory: these options will allow you to choose what you'll import.

**From Beginning To End** does just that. However, if what you're importing is over 500 frames, it will be cut off from the end.

**Selected Range Only** will use the In/Out arrows of the timeline to the right to determine what you're importing. You can use the Play Button and the previous/next frame buttons to fine-tune this.

**Limit to Every # Frames** will shrink the size of your end selection by taking out every *n* frame. Selecting "2" here will take out every second frame, etc.

Keep **Make Frame Animation** checked.

#Step 3: Dealing with what comes out

Photoshop will then spit you back to the main window after importing your GIF and setting it up to be worked with.

Here, Photoshop will import your video as a series of layers; the first frame in the GIF is on the bottom, and the last is on top. Photoshop makes a GIF by showing each frame and then hiding them in sequence, so you are given the illusion of motion.

![Photoshop step 4 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop4.jpg?raw=true)

The key, here, is the **Timeline** window at the bottom of the screen, which will allow us to work with the animation. This is highlighted red in the image below.

![Photoshop step 5 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop5.jpg?raw=true)

If you do not see this window, go to the **Window** menu at the top of the screen and make sure it is visible by checking it.

![Photoshop step 3 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop3.jpg?raw=true)

You can also go to **Window > Workspace > Reset Essentials** if you want in order to make it look exactly like mine in the screenshot. You'll then have to go to **Window > Timeline** in order to make it show up, though.

#Step 3b: Resizing our image (optional)

There are two instances where we can resize our image, and which we use depends on both the power of our computer and the size of our intial upload. Basically we ask ourself: "do I know how big the GIF needs to be, and do I know if it will fit my space requirement at that size?"

If so, we can resize it now. If not, we'll do it before we save the image in another dialog.

Pressing "**CTRL+ALT+I**" or "**⌘+ALT+I**" enters the "Image Size" dialog, which can resize your image. You can also go to **Image > Image Size** if these keyboard shortcuts don't work.

![Photoshop step 6 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop6.jpg?raw=true)

From here you can change the size of your GIF. Keep in mind, the larger the size is, the bigger the end **file** size will be.

For Twitter, you need to keep the file size **under** 15MB. For this size (and for a GIF of a few seconds) I usually choose 500px wide. For other services, you will have to choose other sizes.

This will resize our GIF, and it will be reflected in Photoshop.

![Photoshop step 7 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop7.jpg?raw=true)

Learn more about why this matters [here](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#resizing-our-image---why-reprocessing-matters).

#Step 4: Saving our GIF

Once our GIF is the size and length we need it to be, we can move on to producing a finished product. This assumes that you've gone through steps that you can find in the [Optional Steps and Tweaking](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#other-optional-steps-and-tweaking-before-saving) section below; these include things like color correcting and trimming off frames that don't need to be there.

Primarily we want to work within the "Save For Web" dialog, because GIFs were an image format meant to be placed on the web. In later versions of Photoshop (Creative Cloud 2015 and later) this can be found in the **File > Export** menu, but in earlier versions, you'll find it in **File > Save For Web**. Either way, I usually access it by pressing **CTRL/⌘+ALT+SHIFT+S**.

![Photoshop step 12 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop12.jpg?raw=true)

As you can see, our GIF shows up in the left portion, and it's already been processed a little. This is where the majority of tweaking is going to happen in order to make sure that the GIF is within our desired specifications.

Below I'll be highlighting bits of what all these options mean.

![Photoshop step 13 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop13.jpg?raw=true)

In the top-right of this box (highlighted in red, above) you'll see a dropdown menu that determines the file format of your exported image. You want to make sure it's a GIF; if you're loading this up for the first time it might be a JPEG or PNG, and if you save it, it won't animate.

In the top dropdown, you'll be able to choose from Photoshop's presets for quality ("GIF 128 Dithered", etc). We'll be going into those more later.

![Photoshop step 14 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop14.jpg?raw=true)

Highlighted above is where you'll see two important pieces of information: the **file format** (which we want to be "GIF") and the **file size**. Again, the size depends on the place you're putting it: on Twitter, you can upload GIFs up to 15MB, but on other services (and other services that post to Twitter), that might be greatly reduced. 

The bottom text in the image ("1623 sec @ 56.6Kbps") will show how long it will take to download at certain Internet speeds. These are largely antiquated and assume you're embedding these onto a page. For Twitter, the service will be adding compression in order to reduce time further.

##Optimizing our GIF - why settings matter

The "Save For Web" dialog is often intimidating because it offers so many settings to tweak. However, this is the nature of the beast, as making a good GIF is often a fight to maintain good quality while having a manageable size.

When you get a good idea of what each setting does to the finished GIF, you can figure out what you want to focus on. For instance, the more colors a GIF has the bigger it's going to be; below, you can see the difference between a GIF with 128 colors vs one with 64 — the file size lowers by nearly 2MB.

![128 Colors](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/128colors.jpg?raw=true)

128 Colors - 8.754MB

![64 Colors](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/64colors.jpg?raw=true)

64 Colors - 6.888MB (and a bit less detail)

##Resizing our image - why reprocessing matters

Earlier in the tutorial I wrote about why you'd want to resize your GIF in Photoshop instead of the Save For Web Dialog. You can do the latter by checking out the highlighted boxes below:

![Photoshop step 21 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop21.jpg?raw=true)

There are two reasons why I like making sure the GIF is the size it needs to be **before** entering Save For Web:

1. If you enter Save For Web with a huge GIF (this video imported into Photoshop at 720p) it assumes you want to make it that size initially. Rendering large GIFs (like, we're talking 50+ MB here) takes *forever*, and messes with your work flow.
2. Every time you tweak the size values in Save For Web, the GIF will need to re-process itself, which can take time. This seems to take less time in [the the other method](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-3b-resizing-our-image-optional).

If I can help it, I don't like resizing my GIF in Save For Web due to this reprocessing. If something's coming out at 16MB and knocking it down 50px will put it under the 15MB that I need for Twitter, I'll usually do it here. Otherwise, I'll resize in Photoshop (rather than Save For Web) in order to preserve workflow.

##Comparing changes using 2/4-Up

By clicking the tabs for "2-UP" and "4-UP" at the top-left of the screen, we can see what different settings will do to our GIFs. Clicking on a square will select that window to be modified; any changes you make to the settings will **only change that square**, allowing you to compare sizes and quality.

![Photoshop step 18 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop18.jpg?raw=true)

Above you can see where to click to get into this view, and you can also see a darker grey box around the square I'm currently selecting (the red highlighted box shows where to look for it).

As you can see, each square has their own details to show what's different about them at a glance. The top-left is the original GIF, the top-right is 32 colors with no dither (2.167MB), the bottom-left is 64 colors with 88% dither (6.888MB) and the bottom-right is 128 colors with 88% dither (8.754MB).

Again, this is a great way to see what these changes actually do in relation to each other, and how that affects your finished product. Clicking into each one of the squares will change the settings in the right pane, and the previews will be affected as you change them in turn.

##Custom settings - what they mean

###Color reduction 

Part of what takes up space in a GIF is the data pertaining to color. Since a GIF moves (and lighting shifts with it), it's going to have a lot more colors that a static image. 

A GIF generates these colors by generating a **table**. How it does this is going to affect its size and how the image actually looks. Both color reduction and dithering (see below) will optimize your GIF further, but may affect its quality.

Again, it's a matter of what you're willing to compromise and what the GIF is for.

Below you'll find the exactly same preset, each with less colors. Top-left is 32, top-right is 64, bottom-left is 128 and bottom-right is 256.

![Color comparisons](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/colorcomparison.jpg?raw=true)

When we run them, we can see the level of difference between the examples, including how little "extra" color matters when going from 128 to 256.

Notice how the subject looks relatively the same in the 64, 128 and 256 color examples; since he is the main thing we want to be focusing on, it becomes an acceptable compromise to sacrifice clarity of background elements (like the wall) for size in this case.

![Color comparisons 2](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/colorcomparison2.jpg?raw=true)

However, in other instances, you may need that extra clarity in order to show what you're trying to portray. Your mileage may vary.

###Dithering

In the context of GIF-making, dithering is a technique to smoothen the trandition between colors when the GIF can only use a set amount. Dithering essentially "smooths" the transition between colors by adding dots of alternating colors in order to mask it somewhat.

For example, compare these two images:

![Dithering example](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/dither.jpg?raw=true)

The top one has dithering at 88%, the bottom has 0%. With the bottom image, we can see how much more "blocky" or "splotchy" the colors look in the background, since they are not using dots in order to mask the transition. This also carries over to when the graphic is in motion, as it can be distracting or look unprofessional.

However, the tradeoff for dithering is that the file size increases. In the above example, 0% dither means a file size of 4.962MB, while 88% dithering increases it to 8.75MB.

![Dithering example2](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/dither2.jpg?raw=true)

In a four-way comparison, each of these images has a different amount of dithering. Top-left is 25%, top-right is 50%, bottom-left is 75%, bottom-right is 100%. Note the different file sizes, as well.

You can mostly see the difference in quality around where subtle color changes define detail: the shadows on his skin, and the background wall. Lighting tends to demand more colors due to the variety of shadows it casts, which makes dithering useful in animating real life or detailed shots.

In the options menu, you can choose which algorithm the image is dithered with (Diffusion/Pattern/Noise). Below you can see how each looks: top-left is original, top-right is Diffusion, bottom-left is pattern, bottom-right is Noise.

![Dithering example3](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/dither3.jpg?raw=true)

From [the Adobe knowledge base article on this](http://help.adobe.com/en_US/creativesuite/cs/using/WSC7A1F924-DD38-49b4-B84B-EFF50416C860.html#WSE07483CE-5D9F-4764-AA48-9DF708AD8479):

* Diffusion Applies a random pattern that is usually less noticeable than Pattern dither. The dither effects are diffused across adjacent pixels.
* Pattern Applies a halftone-like square pattern to simulate any colors not in the color table.
* Noise Applies a random pattern similar to the Diffusion dither method, but without diffusing the pattern across adjacent pixels. No seams appear with the Noise dither method.

It is worth noting that only Diffusion will allow you to adjust how much dithering is used in your GIF.

The Transparency checkbox allows you to use transparency to aid in dithering; this will decrease file size because (as far as I know) you won't need extra colors to make up for what can be done with it. Again, you can choose the algorithm you use for this similarly to above.

###Web Snap and Lossy

Both of these options involve how much leeway your GIF is given to reduce data by selectively discarding it. The more lossy an image is, the more static or "noise" is allowed to happen, which reduces clarity and file size.

![lossy example](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/lossy.jpg?raw=true)

The same goes for Web Snap, which will adjust colors to be close to [Web Safe colors](https://en.wikipedia.org/wiki/Web_colors#Web-safe_colors) (which take up less file space in the GIF) at the expense of accuracy through dithering.

![Web Snap example](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/websnap.jpg?raw=true)

You can note the color table on the right side of the settings dialog: there are fewer colors there, and all of them are Web Safe.

###Saving custom settings

By clicking on the menu in the top right of this window **before** we save the image, we can store these custom settings we've made for ourself for later. This means less worrying and an increased workflow later, especially if we're going to be making the same type of GIF over and over.

![custom settings](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/customsettings.jpg?raw=true)

###Looping once vs forever

If for some reason you want your GIF to only loop once, you can do so from the dropdown below.

![loop settings](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/loop.jpg?raw=true)

# Step 5: Finishing up

Once you're comfortable with how your GIF looks, you can click "Save...", give it a name, and you're finished! Woo!

#Other optional steps and tweaking before saving

I originally had these sections as part of the bigger guide as their own steps, but realized that you may not need to use them in every situation. Consider this an "odds and ends" collection; not everything you're going to use with GIFs is here, but most of the things I've run across are.

##Removing frames

After we've got our video in Photoshop as a GIF, there's a couple things we can do to it, and most of them are from the Timeline window.

![Photoshop step 8 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop8.jpg?raw=true)

I'll be highlighting a bunch of the features on this screenshot as we use them, but this is the left side of the Timeline window. However, another feature we'll need will be way on the **right** side of it, highlighted here in red.

![Photoshop step 9 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop9.jpg?raw=true)

This menu allows us to do a number of things with the frames of the animation. Primarily, I am in this menu to *remove* frames. This video wasn't trimmed properly, so there's a few frames that I want removed at the end in order to make it loop better.

![Photoshop step 10 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop10.jpg?raw=true)

I can highlight frames that I don't want with a click, CTRL/⌘ click (for multiple frames) or SHIFT click (for a linear selection) and then...

![Photoshop step 11 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop11.jpg?raw=true)

...go to the menu above and click "**Delete Frames**" in order to remove them.

##Color correction and adding overlay text/images

In order to adjust hue, saturation or any other color options, you can do it the normal way as you would in Photoshop. However, you have to make sure that your adjustments are on top of all the other layers.

[Before](https://github.com/MattDemers/tutorials/blob/master/making-gifs.md#step-3b-resizing-our-image-optionalR) we said that Photoshop imports the video frames as a stack of layers; this is key because we need to affect *all* the layers in the stack, not just one of them.

![](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/layers1.jpg?raw=true)

By scrolling to the top of the layers stack and **then** adding what we want, we can put our layer on the top of all the frames and have it affect everything.

This applies to adding adjustments to color through **Image > Adjustments** or creating a new layer for text and transparent images. Because the layers we're adding have a transparent background, the frames below it can change and have it not affect what's on top.

####As a word of advice, **I strongly suggest you do this in a video editing software** before you import the video to Photoshop. It is much easier than having to ensure consistency for every single frame of your animation, and saves a lot of time.

###Ensuring consistency

The danger to this comes from the fact that **every frame in the animation stores its own position and visibility data for other layers**. This means that if your overlay text is in a different position when Frame 1 is selected in the "Timeline" window than when Frame 2 is selected, it will animate and change places.

For example:

![](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/frame1.jpg?raw=true)

Here I have Frame 1 selected in the Timeline window (red highlight at bottom). I then type in text that I want to show up over everything (purple highlight).

Then I click over to Frame 228, and decide that I want the text somewhere else, so I move it.

![](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/frame2.jpg?raw=true)

When I animate the image, Frame 1 will have the text at the *old* location, because that's where it assumes I want it. **This also applies to visibility (whether it's hidden or showing) and any kind of styling on the layer**.

Thankfully, Photoshop has a way of making sure I don't have to go through each of the 228 frames of this animation and change the text's position.

![](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/unify.jpg?raw=true)

At the top of the "Layer" window (purple highlight) I have the ability to **unify** how the layer is portrayed across all frames. From left to right:

* The pin with the lock ensures position stays consistent
* The eye with the lock ensures visibility stays consistent
* The "fx" with the lock ensures layer style stays consistent
* "Propogate Frame 1" allows changes made a frame carry over to all others after it

Please keep in mind that every time you click a new frame in the Timeline window you are working on a separate part of your animation.

##Increasing pause between frames

Increasing the amount of time a frame spends on the screen became important to me when I started to reach the uppet limit of spacethe a GIF could work with. As I mentioned before, Photoshop can only work with 500 frames at maximum, so having 50 or a 100 that are just the same frame frozen (like say, in a pause) is a waste of space.

![](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/pause.jpg?raw=true)

Each frame, thankfully, has its own menu to adjust the amount of time that the frame spends visible before it moves on to the next one. I believe that the video import (based on the FPS of your video) will determine its default value; from there you can adjust as needed.

I used this when I wanted to annotate esports plays, as I would pause for a couple seconds to show what was going on. 

![](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/lcs.gif?raw=true)

By setting the GIF frame itself to freeze for two seconds (and then edit in text, like I explained above) I could save valuable time and space within my Photoshop work environment.

#Wrapping it all up

Thanks for reading this monster of a guide; I didn't think it would be this long, but hey, these things are important.

I'm sure a lot of you are going to come away from this thinking "man, why don't we just move over to webm, already?"

The thing is, I'd love for that to happen, but the Internet is at a weird place right now where standards are being changed and people still have to develop for older technologies used by people who may not know how to make sure they have the most efficient experience.

Making GIFs is like developing for Internet Explorer: we don't want to do it, but there's going to be someone *somewhere* still using it. It just so happens that that "someone" is a huge amount of web traffic — too big to ignore.

If you have any feedback for this guide, feel free to let me know by clicking on the "issues" tab at the top of the page. If all else, [you can follow me on Twitter](http://twitter.com/mattdemers).

---

The MIT License (MIT)
Copyright (c) 2016 Matt Demers

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
