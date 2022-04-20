## Included frames/graphics and quick guide

* "Dimensions: Inner" means the transparent rectangle inside the frame. This is where you'd fit your content, webcam, or chat.
* "Dimensions: Total" means the image's whole dimensions.
* All content should be placed at `14X, 42Y` on a layer below the frame. More detailed instruction can be found below.

|Label|Dimensions (Inner)| Dimensions (Total)| Notes|
|---|---|---|---|
| **Content Windows**   | ---   | ---   | ---  |
| 3:2 Gameplay Window   | 1536w x 1024h  |  1564w x 1080h | Used for Gameboy Advance, and two portrait (ie, rotated) Nintendo DS windows, side-to-side (used for Hotel Dusk).  |
| 4:3 Gameplay Window   | 1365w x 1024h  |  1393w x 1080h | Used for Nintendo 64, PS1, and other pre-HD games. Also useful for the Nintendo DS (not 3DS), as they use 2x 4:3 displays. The bottom screen of the 3DS is still 4:3, but the top is 15:9; you can use the 16:9 window if you want and have some black bars on the left/right.  |
| 4:6 (2:3) Gameplay Window   | 683w x 1024h  | 711w x 1080h  | Used for landscape Nintendo DS screens, placed one on top of each other. Both are 4:3.  |
| 8:7 Gameplay Window   | 1170w x 1024h  | 1198w x 1080h  | Used for Genesis/SNES, but has some issues as not all games made for those systems fit 10:9 exactly. May have issues pertaining to cropping or need custom solutions (black bars, etc)  |
| 10:9 Gameplay Window   | 1138w x 1024h  | 1166w x 1080h  | Used for Game Boy and Game Boy Color; both have the same resolution. |
| 16:9 Gameplay Window   | 1820w x 1024h  | 1848w x 1080h  | Usually you would use a full-screen scene for a full-screen game (and just put a frame with a webcam on top), but if you want a window, it's here.  |
| Browser Window   | 1842w x 998h  | 1870w x 1055h  | A bit wonky because I'm assuming you've maximized the browser, not-fullscreened it. On Windows 10 that means you have a bar at the bottom taking up some space. If preferred, use a 16:9 gameplay window with a fullscreen browser if it matters that much to you.  |
| **Webcam Windows**   | ---  | ---  | ---  |
| 4:3 Webcam Window   | 1365w x 1024h  | 1393w x 1080h  | More useful if you need a more square/less-wide webcam window.  |
| 16:9 Webcam Window   | 1920w x 1024h  | 1848w x 1080h  | Will fit most default webcam feeds, uncropped.  |
| **Chat Windows**   | ---  | ---  | ---  |
| 1:2 Chat Window   | 512w x 1024h  | 540w x 1080h  | Tall and thin window for chat.  |
| 2:1 Chat Window    | 1892w x 946h  |  1920w x 1002h | Shorter, wider window for chat.  |
| 5:6 Chat Window   | 853w x 1024h  | 881w x 1080h  | Taller box for chat, better layered under other windows.  |

## Detailed Instructions

### Glossary

"**Source**" - Elements in OBS/Xsplit. This manual is written assuming you're using OBS. A source can be an image, video, browser, etc. It is the thing you add to your stream by clicking "Add" and then what you're looking to add.

"**Aspect Ratio**" - A simplified expression of the dimensions of a monitor or window. For instance, a 1080p monitor (1920 px wide, 1080 px tall) has a "16:9" aspect ratio because proportionally, it can't be reduced further. A "4:6" aspect ratio can be reduced down to "2:3". Fractions!

"**Resolution**" - The width by height of a window or monitor. Width will always go first here.

"**Crop**" - Using [OBS' Crop Filter](https://streamshark.io/obs-guide/cropping-a-layer) or [Transform Settings](https://www.youtube.com/watch?v=-imnE05uV0U), you can shave off pixels from the Top, Bottom, Left or Right of a source.

"**X,Y**" - X is horizontal distance, Y is vertical distance; the origin point (0,0) is the top-left corner of an image or your screen. If something is at "10,20" coordinates, it means that it's 10 pixels to the right from the top-left corner, and 20 pixels down from the top-left corner.

### Basics

All the images and windows in this project start their top-left corner at 14X,42Y. The 14px compensates for the left border, and the 42px compensates for the top border and the "title bar".

When setting this up in OBS. You will likely layer the windows as such (top to bottom):

1. Image/frame (the PNGs packaged here)
2. Content source (game, chat, webcam, etc)
3. Background (optional, mostly for chat)

You can then select these sources in OBS and click ``Group Selected Items``. This allows you to move both or all three elements at once, keeping them together.

![Image](https://i.imgur.com/OEjBssW.png)

For extra protection, **click the lock** beside each source, **but not the group itself**; you'll still be able to move/resize the group, and not ruin your setup. To make hiding/revealing groups easier, **make sure to keep sources inside a group visible**; they'll hide themselves appropriately when you hide the parent group.

![Image](https://i.imgur.com/yxbCRWg.png)

*The folder is unlocked, so it can be moved and resized. The things *in* the folder are locked, so they aren't accidentally modified. Everything in the image is visible, but if you want to hide the whole group at once, you would click the **topmost** eye icon*.

## Non-Gaming Windows

Some notes:

1. The chat windows are big, so the font setting is big to play well with scaling.
2. My experience is with Streamlabs and StreamElements, and at least both of those sites will work. **I offer no support for other services, or support for SL/SE beyond what I've included**; it's on you to be able to figure out.
3. I've included some basic custom CSS below to make things look decent, but you're on your own for more custom CSS for additional fonts, etc.

After adding the frame to OBS, you'll highlight it and press "Ctrl+E" or right-click it, click `Transform > Edit Transform`. You'll get to a window like this.

![Image](https://i.imgur.com/H5MCPiF.png)

---

### 16:9 Browser

* MattOS Viewport Size: 1820x998
* OBS `Transform` Position: 14x42y
* Browser size is assumed to be **fullscreen** on a 16:9 monitor with a standard Windows 10 taskbar.

### Maximized Browser

* Viewport Size: 1842 x 998
* OBS `Transform` Position: 14x42y
* Browser size is assumed to be maximized (**not fullscreened**) on a 16:9 monitor with a standard Windows 10 taskbar.

### 5:6 Chat (Tall)

* When you first add a Browser Source, you'll be asked for a height and width: use the below "Viewport Size" values. If you need to change/add this later, double click on the browser source in the OBS list.
* Viewport Size: 853x1024
* OBS `Transform` Position: 14x42y
* Suggested StreamElements Font Size: 32pt
* Chat windows **require** an OBS Color Source (Add > Color Source) behind them, the same size as the Window Size. Otherwise, there will be no background to your chat, and affect readability. It should be sized ``853x1024`` in this case, and placed at 14X, 42Y to fit into the window.
* To make the Color Source transparent, either adjust the ```Alpha Channel``` field in the source's options, or Right Click the source in the main OBS window, go to ``Filters``, then add a ``Color Correction`` filter. Change the opacity with the slider there.

### 2:1 Chat (Wide)

* When you first add a Browser Source, you'll be asked for a height and width: use the below "Viewport Size" values. If you need to change/add this later, double click on the browser source in the OBS list.
* Viewport Size: 1892x946
* OBS `Transform` Position: 14x42y
* Suggested StreamElements Font Size: 56pt
* Chat windows **require** an OBS Color Source (Add > Color Source) behind them, the same size as the Window Size. Otherwise, there will be no background to your chat, and affect readability. It should be sized ``1892x946`` in this case, and placed at 14X, 42Y to fit into the window.
* To make the Color Source transparent, either adjust the ```Alpha Channel``` field in the source's options, or Right Click the source in the main OBS window, go to ``Filters``, then add a ``Color Correction`` filter. Change the opacity there.

#### 1:2 Chat (Tall)

* When you first add a Browser Source, you'll be asked for a height and width: use the below "Viewport Size" values. If you need to change/add this later, double click on the browser source in the OBS list.
* Viewport Size: 512x1024
* OBS `Transform` Position: 14x42y
* Suggested StreamElements Font Size: 32pt
* Chat windows **require** an OBS Color Source (Add > Color Source) behind them, the same size as the Window Size. Otherwise, there will be no background to your chat, and affect readability. It should be sized ``1892x946`` in this case, and placed at 14X, 42Y to fit into the window.
* To make the Color Source transparent, either adjust the ```Alpha Channel``` field in the source's options, or Right Click the source in the main OBS window, go to ``Filters``, then add a ``Color Correction`` filter. Change the opacity there.


#### StreamElements Chat Custom CSS:

If you use StreamElements for your chat, right click on your chat's browser source **in OBS** and delete everything in ``Custom CSS``.

![Image](https://i.imgur.com/o6JEiiF.png)

Replace it with the below code.

```
.chat-line {
padding: 0px 10px;
}

.chat-line .badge {
vertical-align: middle;
```
* The ``.chat-line`` code will keep your chat lines from butting up against the side of the frame.
* The ``.chat-line .badge`` code will vertically align your chat badges (Turbo, Mod, etc).

#### StreamLabs Chat Custom CSS:

If you use StreamLabs for your chat widget, delete everything in the Custom CSS box, and replace it with the code below.

I've found the "Chunky" theme in StreamLabs works best with this, with the animations disabled. The default font size should be increased; 30px seems to work.


```
.#log .meta {
    width: 35%;
    text-align: right;
    padding-right: 0.5em;
    white-space: nowrap;
    text-overflow: visible;
    overflow: visible;
}

#log .message,#log .meta {
    vertical-align: top;
    display: inline;
    padding-bottom: 0.1em;
}


#log .message {
    word-wrap: break-word;
    width: 65%;
    padding-left: 0.5em;
}

```

This will fix Streamlabs hiding longer messages or usernames behind "..." shorteners, and also fix some display issues.

Save your settings, and you should be good to go.

#### CSS Support

I offer no support for CSS issues or further customization. That's on you to fix.

## Game or Webcam Scenes

### Common Setup:

1. Load the image into OBS as a source by right-clicking on the Preview window, or hitting the "+" in the ``Sources`` pane. Click "Image."
2. Make sure it is "reset" or "fit to screen" (``Ctrl+F`` with the image selected in OBS). In almost all cases, it should reach from top to bottom of a 1080p screen.
3. You'll then add your game, webcam or chat browser source into OBS. Right click it in the Preview window or in the Sources List, then go to ``Transform`` and then ``Edit Transform``. You can also press ``Ctrl+E`` while selecting a source.
3. When you modify your gaming or video source, you're looking to make sure the ``Position`` is ``14`` (first field) and ``42`` (second field). These numbers compensate for the frame around the window, so nothing is cut off. Please making sure ``Positional Alignment`` is ``Top Left``.
4. Your source ``Size`` should always be 1920x1080 if you're playing a game in full screen. The crop values below assume you are, but you're welcome to adjust your own crop to fit, if you're playing in Windowed Mode.
5. ``Bounding Box Type`` should be ``Scale to height of bounds`` unless otherwise noted. ``Alignment in Bounding Box`` can stay at ``Center``.
6. For the ``Crop`` values, put in what you need to for Left and Right, based on what I've put in below, or through your own experimentation. I cannot troubleshoot all window fits, so I am assuming you're playing full screen on a 1080p monitor.
     - If you know your monitor's resolution, go to [Aspect Ratio Calculator](https://andrew.hedges.name/experiments/aspect_ratio/) and place the aspect ratio numbers for a system into ``W1`` and ``H1`` (for example, 4 and 3 for 4:3). Then, put the **height** of your monitor into ``H2`` (for example, ``1200`` for a 1920x1200, 16:10 monitor). Subtract the number generated in ``W2`` from your monitor's **width** (for example, ``1920-1600=320`` for a 16:10 monitor), then divide that number by 2 in order to get how much you need to take off each side (``320/2=160`` cropped from the left and right) to hit the aspect ratio.

An example of a successful adjustment for a webcam cropped to a 4:3 frame. Compare this diagram to the "4:3" instructions below if you're unclear where they go.

![Image](https://i.imgur.com/H5MCPiF.png)

### 4:3 (Nintendo 64/Playstation 1/Playstation 2/GameCube, 480p, Nintendo DS individual screens)

* Assumes the content is running in a 1920w x 1080h, fullscreen window.
* Viewport Size: 1365x1024
* OBS `Transform` Position: 14x42y
* Crop for a window at 1080p full screen: ``1920-1440/2`` = **240px** from each side will get you to 4:3.
* Note for N64: like the SNES, developers added extra black borders to [compensate for overscan](https://gliden64.blogspot.com/2018/05/overscan.html). Unfortunately you can either use your emulator or OBS to crop out the remaining bits.

### 16:9 (Webcam, Gaming, Browser)

* Assumes the content is running in a 1920w x 1080h, fullscreen window.
* Viewport Size: 1820x1024
* OBS `Transform` Position: 14x42y
* If you're playing a game widescreen/full screen, it shouldn't need to be cropped or put in a frame.
* Browser must be fullscreen.
* If you still want to put something in it, or are using a 1080p webcam capture, resize those video sources to 1820x1024. **You do not need to add a Bounding Box for this, since you're not cropping the 16:9 image, only resizing it.**

### 3:2 (Game Boy Advance)

* Assumes the content is running in a 1920w x 1080h, fullscreen window.
* Viewport Size: 1536x1024
* OBS `Transform` Position: 14x42y
* Crop for a window at 1080p full screen: ``(1920-1620)/2`` = **150px** from each side will get you to 3:2.

### 10:9 (Game Boy, Game Boy Color)

* Assumes the content is running in a 1920w x 1080h, fullscreen window.
* Viewport Size: 1138x1024
* OBS `Transform` Position: 14x42y
* Crop for a window at 1080p full screen: ``(1920-1200)/2`` = **360px** from each side will get you to 10:9.

### 8:7 (SNES, Genesis/Master System)

* Assumes the content is running in a 1920w x 1080h, fullscreen window.
* Viewport Size: 1170x1024
* OBS `Transform` Position: 14x42y
* Crop for a window at 1080p full screen: ``(1920-1234)/2`` = **343px** from each side will get you to 8:7.
* However, certain games (Tetris Attack, others) don't run at 8:7 aspect ratio, and removing 343px from each side will cut off game space. Use "Fit To Width" instead of "Fit To Height" and adjust crop as needed manually. Unfortunately because this is a case-by-case basis, this can't be standardized.

### Portrait 2:3/4:6 (Dual Portrait DS screens for Hotel Dusk, etc)

* Assumes the content is running in a 1920w x 1080h, fullscreen window.
* Viewport Size: 1620x1024
* OBS `Transform` Position: 14x42y
* Crop for a window at 1080p full screen: ``1920-1620/2`` = **300px** from each side will get you to 6:4.
* There seems to be a small black line on the left side of the dual screen, likely to correct for overscan. Adjust as needed.
* This layout doesn't account for a gap between the bezels/hinge of the Nintendo DS. Likely will need some tweaking in cropping or at the emulator level to compensate.

## Backgrounds, Clock, and the Taskbar

## The Bottom Menu Bar

* The bottom taskbar should be placed at X0, Y 1080, with the ``Positional Alignment`` being changed from "Top Left" to "Bottom Left".
* The bottom taskbar's `Size` is 1920x50.



The font I use for MattOS is [Pixellari](https://www.dafont.com/pixellari.font) by [Zacchary Dempsey-Plante](https://ztdp.ca). It's 100% free. If you install it on your Operating System, OBS will be able to use it, too.

You can use any number of services to get a working clock on your bar:

1. I use [this option](https://obsproject.com/forum/threads/datetime-digital-clock.113883/) in the form of a Lua script. Install instructions are [here](https://obsproject.com/forum/threads/datetime-digital-clock.113883/post-464271).
2. You can also use [this option](https://www.youtube.com/watch?v=wVbP8GQTLG8) as a browser source (captions on!)
3. Software like [Snaz](https://snaz1.software.informer.com/1.9/) allows you to output the time to a text file.

* The clock's size is 112x30px, but can vary depending on whether you want to use things like 24 hour clock or AM/PM. I use a 28pt font with ``Pixeallari Medium``. My format using "Option 1" above is ``%I:%M%p``.
* Your clock should be placed at 1842X 1060Y with the ``Positional Alignment`` set to "Center."

I offer no support or warranty to these methods; I just know the first one has worked for me.

## Backgrounds

It's pretty simple: make a folder full of images that are the same size as your broadcast's output resolution (example: if you're streaming in 1080p, have a bunch of 1920x1080 images).

Add this folder as an image slideshow in OBS, and **make sure it's the lowest layer in your sources list.**
