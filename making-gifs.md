#Making GIFs with Photoshop

Making GIFs is currently becoming one of the most important things in my toolkit, mostly because they make tweets look better and furnish articles well. However, you need to be careful of both size and content in order to meet space requirements, as the file format is inherently large due to its age and poor optimization.

This can be worked around in certain stages, but sadly people haven't phased GIFs out entirely due to a couple reasons (by my thoughts, at least):

1. They auto-play on Twitter instead of requiring a user to click through. They also play on hover for other services (Tumblr, Facebook, etc)
2. They are accepted by many older services, especially ones that don't accept embedding your own HTML (like Pinterest)
3. GIFV, GFYs and .WebMs have yet to come up with a format that works for everyone

It sounds silly, but even putting one button for people to click (like playing a video or .WebM) might be enough for people *not* to click on it. Sadly, that's how content works sometimes.

#This Guide Requires:

* Photoshop
* Mild video editing

The reason we're using Photoshop instead of some kind of other editor or drag-and-drop GIF maker is because I like to know how big the output GIF is going to be, and have fine-tuning over different things like how fast it runs, what the colors look like, and its end dimensions. If you're in an absolute hurry, sure, you can use one of those services, but you're usually going to have to put up with bad compression, a watermark logo, or something that ultimately looks bad or doesn't fit your needs.

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

**Selected Range Only** will use the In/Out arrows of the timeline to the right to determine what you're importing. YOu can use the Play Button and the previous/next frame buttons to fine-tune this.

**Limit to Every # Frames** will shrink the size of your end selection by taking out every *n* frame. Selecting "2" here will take out every second frame, etc.

Keep **Make Frame Animation** checked.

#Step 3: Dealing with what comes out

Photoshop will then spit you back to the main window after importing your GIF and setting it up to be worked with.

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

#Step 4: Saving our GIF

If our GIF is already the size and length we need it to be, we can move on to producing a finished product. This assumes that you've gone through steps that you can find in the [Optional Steps and Tweaking](#optional-steps-and-tweaking) section below; these include things like color correcting and trimming off frames that don't need to be there.

Primarily we want to work within the "Save For Web" dialog, because GIFs were an image format meant to be placed on the web. In later versions of Photoshop (Creative Cloud 2015 and later) this can be found in the **File > Export** menu, but in earlier versions, you'll find it in **File > Save For Web**. Either way, I usually access it by pressing **CTRL+ALT+SHIFT+S**.

![Photoshop step 12 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop12.jpg?raw=true)

As you can see, our GIF shows up in the left portion, and it's already been processed a little. This is where the majority of tweaking is going to happen in order to make sure that the GIF is within our desired specifications.

Below I'll be highlighting bits of what all these options mean.

![Photoshop step 13 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop13.jpg?raw=true)

In the top-right of this box (highlighted in red, above) you'll see a dropdown menu that determines the file format of your exported image. You want to make sure it's a GIF; if you're loading this up for the first time it might be a JPEG or PNG, and if you save it, it won't animate.

![Photoshop step 14 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop14.jpg?raw=true)

Highlighted above is where you'll see two important pieces of information: the **file format** (which we want to be "GIF") and the **file size**. Again, the size depends on the place you're putting it: on Twitter, you can upload GIFs up to 15mb, but on other services (and other services that post to Twitter), that might be greatly reduced. 

The bottom text in the image ("1623 sec @ 56.6Kbps") will show how long it will take to download at certain Internet speeds. These are largely antiquated and assume you're embedding these onto a page. For Twitter, the service will be adding compression in order to reduce time further.


#Optional Steps And Tweaking

I originally had these sections as part of the bigger guide as their own steps, but realized that you may not need to use them in every situation. Consider this an "odds and ends" collection; not everything you're going to use with GIFs is here, but most of the things I've run across are.

##Removing Frames

After we've got our video in Photoshop as a GIF, there's a couple things we can do to it, and most of them are from the Timeline window.

![Photoshop step 8 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop8.jpg?raw=true)

I'll be highlighting a bunch of the features on this screenshot as we use them, but this is the left side of the Timeline window. However, another feature we'll need will be way on the **right** side of it, highlighted here in red.

![Photoshop step 9 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop9.jpg?raw=true)

This menu allows us to do a number of things with the frames of the animation. Primarily, I am in this menu to *remove* frames. This video wasn't trimmed properly, so there's a few frames that I want removed at the end in order to make it loop better.

![Photoshop step 10 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop10.jpg?raw=true)

I can highlight frames that I don't want with a click, CTRL click (for multiple frames) or SHIFT click (for a linear selection) and then...

![Photoshop step 11 image.](https://github.com/MattDemers/tutorials/blob/master/images/GIF%20Tutorial/Photoshop11.jpg?raw=true)

...go to the menu above and click "**Delete Frames**" in order to remove them.





