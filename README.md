<!doctype html>
<html>
<head>
<title>jquery视差滑块幻灯特效(易烊千玺)</title>
<meta charset="utf-8">
<link rel="stylesheet" type="text/css" href="css/style.css" />
<script src="js/move.js" type="text/javascript"></script>
<script src="js/index.js" type="text/javascript"></script>
</head>
<body>
    <div class="wrapper">
        
    </div>

    <div id="pxs_container" class="pxs_container">
        <div class="pxs_bg">
            <div class="pxs_bg1"></div>
            <div class="pxs_bg2"></div>
            <div class="pxs_bg3"></div>
        </div>
        <div class="pxs_loading">Loading images...</div>
        <div class="pxs_slider_wrapper">
            <ul class="pxs_slider">
                <li><img src="images/07.jpg" alt="First Image" /></li>
                <li><img src="images/02.jpg" alt="Second Image" /></li>
                <li><img src="images/03.jpg" alt="Third Image" /></li>
                <li><img src="images/04.jpg" alt="Forth Image" /></li>
                <li><img src="images/05.jpg" alt="Fifth Image" /></li>
                <li><img src="images/06.jpg" alt="Sixth Image" /></li>
            </ul>
            <div class="pxs_navigation">
                <span class="pxs_next"></span>
                <span class="pxs_prev"></span>
            </div>
            <ul class="pxs_thumbnails">
                <li><img src="images/thumbs/07.jpg" alt="First Image" /></li>
                <li><img src="images/thumbs/02.jpg" alt="Second Image" /></li>
                <li><img src="images/thumbs/03.jpg" alt="Third Image" /></li>
                <li><img src="images/thumbs/04.jpg" alt="Forth Image" /></li>
                <li><img src="images/thumbs/05.jpg" alt="Fifth Image" /></li>
                <li><img src="images/thumbs/06.jpg" alt="Sixth Image" /></li>
            </ul>
        </div>
    </div>
   <div class="footer">
		<div style="text-align:center;clear:both;">
  </div>
<script src="/gg_bd_ad_720x90.js" type="text/javascript"></script>
<script src="/follow.js" type="text/javascript"></script>

<script>
var oLoad = getByClass(document.body, 'pxs_loading')[0];
var oImgBox = getByClass(document.body,'pxs_slider_wrapper')[0];

var imgs = document.getElementsByTagName('img');
for(var i=0;i<imgs.length;i++){
	imgs[i].onload = function()
	{
		oLoad.style.display = 'none';
	}
	oImgBox.style.display = 'block';
}
</script>    

</body>
</html>
