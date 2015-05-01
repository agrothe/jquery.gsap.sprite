# jquery.gsap.sprite
Sprite control plugin for jQuery &amp; GSAP

Demo: http://jsbin.com/quvuzo/6/edit?html,js,output

Usage:

Include dependancies:
```
<script src="//code.jquery.com/jquery-2.1.1.min.js"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/gsap/1.16.1/TweenMax.min.js"></script>
```
Init the plugin and start controlling it:
```
var mark = $(".mark").sprite({
  frameWidth: 24, 
  frameHeight: 70, 
  sheetWidth: 120,
  imageSrc:"https://dl.dropboxusercontent.com/u/6801572/marksprite.png"
});
 
// Pause the sprite
mark.sprite("pause");

// Play the sprite
mark.sprite("play");

// Resume the sprite from where it was paused
mark.sprite("resume");

// Restart the sprite from the beginning
mark.sprite("restart");

// Stop the sprite
mark.sprite("stop");

// Goto first frame (0 indexed) and stop
mark.sprite("seek", 0, true);  

// Goto thrid frame (0 indexed) and stop
mark.sprite("seek", 2, true);

// Goto thrid frame (0 indexed) and continue
mark.sprite("seek", 2, true);

 ```
 
 All Options:
 
Option | Default | Description
------ | ------- | -----------
imageSrc | null | (optional) uses background-image css property otherwise
frameWidth | 100 | pixel width value of each frame as an integer ie. 100 not 100px
frameHeight | 100 | pixel height value of each frame as an integer ie. 100 not 100px
sheetWidth | 1000 | pixel width value of total sprite sheet as an integer ie. 1000 not 1000px
speed | 0.150 | animation speed in milliseconds
timeLine | null | (optional) Timeline object to use instead of internal variable.
TimelineMaxOverride | null | (optional) TimelineMax library, in case of customization
TweenMaxOverride | null | (optional) TweenMax library, in case of customization
