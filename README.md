# PreVideoLoad
Ultralight weight jQuery plugin for load thumb of videos from Vimeo and Youtube and load fully when is needed.

# Starting
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

You can put the script in the bottom (before </body>), but you could see 'ghost' if you insert alternate content in video container.
