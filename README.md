# PreVideoLoad
Ultralight weight jQuery plugin for load thumb of videos from Vimeo and Youtube and load fully when is needed.

The js file size is only 1971 bytes! The css size is 9695 bytes due to base64 images. Use an external image and the css weight will be even less than the js file!

# Features
<ul>
<li>Small filesize</li>
<li>Cross-browser (Tested in IE8 but teorically it works in IE6+)</li>
<li>Easy customization and configuration</li>
<li>Fast page load</li>
</ul>

# Starting
Loading files:

<pre>
&lt;link rel="stylesheet" type="text/css" href="prevideoload.css"&gt;
&lt;script src="jquery-1.11.3.min.js"&gt;&lt;/script&gt;
&lt;script src="prevideoload.js"&gt;&lt;/script&gt;
</pre>

You can put the script in the bottom (before </body>), but you could see 'ghost' if you insert alternate content in video container.

# Example
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;link rel="stylesheet" type="text/css" href="prevideoload.css"&gt;
&lt;script src="jquery-1.11.3.min.js"&gt;&lt;/script&gt;
&lt;script src="prevideoload.js"&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div class="PreVideoLoad PreVimeo" data-videoid="136084530"&gt;Alternate content for non-javascript users&lt;/div&gt;
&lt;div class="PreVideoLoad PreYoutube" data-videoid="yOcPZvFd1k8"&gt;&lt;/div&gt;
&lt;div class="PreVideoLoad PreVimeo" data-videoid="136084531"&gt;&lt;/div&gt;
&lt;div class="PreVideoLoad PreYoutube" data-videoid="yOcPZvFd1k8"&gt;&lt;/div&gt;
&lt;script type="text/javascript"&gt;
$(function(){
	$('.PreVideoLoad').PreVideoLoad();
});
&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

# Options
<ul>
<li>@bool autoPlay (default true): true for play the video after click on the button</li>
<li>@string event (default 'click'): when to load video</li>
<li>@string ytimg (default 0): quality of youtube's video thumbnail. Can be: 0 | 1 | 2 | 3 | default | hqdefault | mqdefault | sddefault | maxresdefault</li>
<li>@string vmimg (default large): quality of vimeo's video thumbnail. Can be: small | medium | large</li>
</ul>

# Setting options
<pre>
var options = {
	autoPlay: false,
	event: 'onmouseover',
	ytimg: 'maxresdefault',
	vmimg: 'small'
};
$('.PreVideoLoad').PreVideoLoad(options);
</pre>

# <a href="http://matyrock.github.io/PreVideoLoad/">Website</a> | <a href="http://matyrock.github.io/PreVideoLoad/demo.html">Demo</a>

# Future features
<ul>
<li>Override defaults by setting options to the divs</li>
<li>Title loading</li>
<li>Load the video when user scroll on it</li>
<li>Responsive width and height!</li>
<li>And many more!</li>
</ul>
