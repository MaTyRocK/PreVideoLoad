**Note: I made this plugin when I was still learning jQuery and JavaScript in general. You should NOT use this! There are lots of good libraries that do the same but 1000x better.**

-----

# PreVideoLoad
Ultralight weight jQuery plugin for load thumb of videos from Vimeo and Youtube and load fully when is needed.

The js file size is only **1971 bytes**! The css size is 9695 bytes due to base64 images. **Use an external image and the css weight will be even less than the js file!**

## <a href="http://matyrock.github.io/PreVideoLoad/demo.html">Demo</a>

# Features
<ul>
<li>Small filesize</li>
<li>Cross-browser (Tested in IE8 but teorically it works in IE6+)</li>
<li>Easy customization and configuration</li>
<li>Fast page load</li>
</ul>

# Starting
Loading files:

``` html
<link rel="stylesheet" type="text/css" href="prevideoload.css">
<script src="jquery-1.11.3.min.js"></script>
<script src="prevideoload.js"></script>
```

You can put the script in the bottom (before `</body>`), but you could see 'ghost' if you insert alternate content in video container.

# Example
``` html
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" type="text/css" href="prevideoload.css">
<script src="jquery-1.11.3.min.js"></script>
<script src="prevideoload.js"></script>
</head>
<body>
<div class="PreVideoLoad PreVimeo" data-videoid="136084530">Alternate content for non-javascript users</div>
<div class="PreVideoLoad PreYoutube" data-videoid="yOcPZvFd1k8"></div>
<div class="PreVideoLoad PreVimeo" data-videoid="136084531"></div>
<div class="PreVideoLoad PreYoutube" data-videoid="yOcPZvFd1k8"></div>
<script type="text/javascript">
$(function(){
	$('.PreVideoLoad').PreVideoLoad();
});
</script>
</body>
</html>
```

# Options
- @bool `autoPlay` (default `true`): true for play the video after click on the button
- @string `event` (default `click`): when to load video
- @string `ytimg` (default `0`): quality of youtube's video thumbnail. Can be: 0 | 1 | 2 | 3 | default | hqdefault | mqdefault | sddefault | maxresdefault
- @string `vmimg` (default `large`): quality of vimeo's video thumbnail. Can be: small | medium | large

# Setting options
``` javascript
var options = {
	autoPlay: false,
	event: 'onmouseover',
	ytimg: 'maxresdefault',
	vmimg: 'small'
};
$('.PreVideoLoad').PreVideoLoad(options);
```

# Future features
<ul>
<li>Override defaults by setting options to the divs</li>
<li>Title loading</li>
<li>Load the video when user scroll on it</li>
<li>Responsive width and height!</li>
<li>And many more!</li>
</ul>
