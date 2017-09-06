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



*{
	margin:0;
	padding:0;
}
body{
	font-family:"Trebuchet MS", "Myriad Pro", Arial, sans-serif;
	font-size:14px;
	background:#222;
	color:#333;
	overflow-x:hidden;
}
h1{
	font-size:56px;
	color:#ccc;
}
h2{
	font-size:20px;
	padding:10px 0px 10px 0px;
	margin:15px 0px 20px 0px;
	color:#999;
	text-shadow:0 0 3px 5px #000000;
}
a{
	color:#555;
	text-decoration:none;
}
a:hover{
	color:#222;
}
p{
	padding:5px 0px;
}
.wrapper{
	width:960px;
	margin:10px auto;
}
.clear{
	clear:both;
}
.footer{
	text-align:center;
	width:100%;
	padding:20px 0px;
	clear:both;
	margin-top:30px;
	color:#666;
}
.footer a{
	margin:0px 20px;
}
.footer a:hover{
	color:#666;
}
/* Slider Style */
.pxs_container{
	width:100%;
	height:420px;
	position:relative;
	border-top:7px solid #333;
	border-bottom:7px solid #333;
	overflow:hidden;
	-moz-box-shadow:0px 0px 7px #000;
	-webkit-box-shadow:0px 0px 7px #000;
	box-shadow:0px 0px 7px #000;
}
.pxs_bg{
	background:url('bg.png') top left;
}
.pxs_bg div{
	position:absolute;
	top:0px;
	left:0px;
	width:7584px;
	height:420px;
	background-repeat:repeat;
	background-position:top left;
	background-color:transparent;
}
.pxs_bg .pxs_bg1{
	/*background-image:url(bg1.png);*/
	/*left negative 1/8 of*/
	background:url(../images/2.png) repeat-x left top ;
}
.pxs_bg .pxs_bg2{
	background:url(../images/1.png) repeat-x -200px 20px;
	/*left negative 1/4 of*/
}
.pxs_bg .pxs_bg3{
	/*background-image:url(bg3.png);*/
	/*left negative 1/2 of*/
	background:url(../images/3.png) repeat-x left 140px;
}
.pxs_slider_wrapper{
	display:none;
}
.pxs_container ul{
	margin:0px;
	padding:0px;
	list-style:none;
}
ul.pxs_slider{
	position:absolute;
	left:0px;
	top:0px;
	height:420px;
}
ul.pxs_slider li{
	height:420px;
	float:left;
	position:relative;
}
ul.pxs_slider li img{
	display:block;
	margin:35px auto 0px auto;
	-moz-box-shadow:0px 0px 7px #222;
	-webkit-box-shadow:0px 0px 7px #222;
	box-shadow:0px 0px 7px #222;
	border: 8px solid transparent;
	-moz-border-radius:4px;
	-webkit-border-radius:4px;
	border-radius:4px;
}
ul.pxs_thumbnails{
	height:35px;
	position:absolute;
	top:320px;
	left:50%;
}
ul.pxs_thumbnails li{
	position:absolute;
	display:block;
}
ul.pxs_thumbnails li img{
	border: 5px solid #FFFFFF;
	-moz-box-shadow:1px 1px 7px #555;
	-webkit-box-shadow:1px 1px 7px #555;
	box-shadow:1px 1px 7px #555;
	cursor:pointer;
	display:block;
	opacity:0.7;
}
ul.pxs_thumbnails li.selected img{
	opacity:1.0;
}
.pxs_navigation span{
	position:absolute;
	width:30px;
	height:60px;
	-moz-box-shadow:0px 0px 2px #000;
	-webkit-box-shadow:0px 0px 2px #000;
	box-shadow:0px 0px 2px #000;
	top:145px;
	opacity:0.6;
	-moz-border-radius:4px;
	-webkit-border-radius:4px;
	border-radius:4px;
	cursor:pointer;
}
.pxs_navigation span:hover{
	opacity:0.9;
}
.pxs_navigation span.pxs_prev{
	background:#000 url(../images/prev.png) no-repeat center;
}
.pxs_navigation span.pxs_next{
	background:#000 url(../images/next.png) no-repeat center;
}
.pxs_loading{
	color:#fff;
	font-size:20px;
	background:#333 url('ajax-loader.gif') no-repeat 10px 50%;
	-moz-border-radius:15px;
	-webkit-border-radius:15px;
	border-radius:15px;
	opacity:0.7;
	width:180px;
	position:absolute;
	top:150px;
	left:50%;
	margin-left:-90px; padding-left:50px; padding-right:15px; padding-top:15px; padding-bottom:15px
}



function getStyle(obj, attr)
{
	if(obj.currentStyle)
	{
		return obj.currentStyle[attr];
	}
	else
	{
		return getComputedStyle(obj, false)[attr];
	}
}
function $(id)
{
	return document.getElementById(id);
}

function setStyle3(obj, name, value)
{
	obj.style['Webkit'+name.charAt(0).toUpperCase()+name.substring(1)]=value;
	obj.style['Moz'+name.charAt(0).toUpperCase()+name.substring(1)]=value;
	obj.style['ms'+name.charAt(0).toUpperCase()+name.substring(1)]=value;
	obj.style['O'+name.charAt(0).toUpperCase()+name.substring(1)]=value;
	obj.style[name]=value;
}

function getByClass(oParent,sClass)
{
	var aEle = oParent.getElementsByTagName('*');
	var aResult = [];
	var re=new RegExp('\\b'+sClass+'\\b', 'i');
	
	for(var i=0; i<aEle.length;i++)
	{
		if(aEle[i].className.search(re)!=-1)
		{
			aResult.push(aEle[i]);
		}
	}
	return aResult;
}

function startMove(obj, json, fnEnd)
{
	clearInterval(obj.timer);
	var attr;
	obj.timer=setInterval(function (){
		
		var bStop=true;		//是不是都到了，假设所有的都到了
		
		for(attr in json)
		{
			var iCur=0;
			
			//取当前位置
			if(attr=='opacity')
			{
				iCur=Math.round(parseFloat(getStyle(obj, attr))*100);
			}
			else
			{
				iCur=parseInt(getStyle(obj, attr));
			}
			
			//算速度
			var iSpeed=(json[attr]-iCur)/8;
			iSpeed=iSpeed>0?Math.ceil(iSpeed):Math.floor(iSpeed);
			
			//到没到
			
			if(attr=='opacity')
			{
				obj.style.filter='alpha(opacity:'+(iCur+iSpeed)+')';
				obj.style.opacity=(iCur+iSpeed)/100;
			}
			else
			{
				obj.style[attr]=iCur+iSpeed+'px';
			}
			
			if(iCur!=json[attr])
			{
				bStop=false;
			}
		}
		
		if(bStop)
		{
			clearInterval(obj.timer);
			if(fnEnd)
			{
				fnEnd();
			}
		}
		//alert(obj.offsetHeight);
	}, 30);
}



window.onload = function()
{
	var oImgBox = getByClass(document.body,'pxs_slider_wrapper')[0];
	var oImg = getByClass(document.body,'pxs_slider')[0];
	var aLi = oImg.getElementsByTagName('li');
	var aImg = oImg.getElementsByTagName('img');
	
	//各种背景
	var bg1 = getByClass(document.body,'pxs_bg1')[0];
	var bg2 = getByClass(document.body,'pxs_bg2')[0];
	var bg3 = getByClass(document.body,'pxs_bg3')[0];
	
	var oPrev = getByClass(document.body,'pxs_next')[0];
	var oNext = getByClass(document.body,'pxs_prev')[0];
	
	var oImg_sm = getByClass(document.body,'pxs_thumbnails')[0];
	var aImg_li = oImg_sm.getElementsByTagName('li');
	var aImg_sm = oImg_sm.getElementsByTagName('img');
	
	var iNow = 0;
	
	oImg.style.width = aLi.length * document.documentElement.clientWidth + 'px';
	
	for(var i=0; i<aLi.length;i++)
	{
		aLi[i].style.width = document.documentElement.clientWidth + 'px';
	}
	
	oPrev.style.left = document.documentElement.clientWidth /2 + aImg[0].offsetWidth /2  - oPrev.offsetWidth - 14 + 'px';
	oNext.style.left = document.documentElement.clientWidth /2 - aImg[0].offsetWidth /2  + oPrev.offsetWidth - 15 + 'px';
	
	oImg_sm.style.width = aImg[0].offsetWidth + 'px';
	oImg_sm.style.marginLeft = - aImg[0].offsetWidth/2 + 'px'
	
	for(var i=0;i<aImg_sm.length;i++)
	{
		aImg_li[i].index = i;
		var ran = Math.random() * 40 - 20;
		var cliWidth = (oImg_sm.offsetWidth - aImg_li[0].offsetWidth*aImg_li.length)/(aImg_li.length+1);
		aImg_li[i].style.left = cliWidth + i*(cliWidth+aImg_li[i].offsetWidth) + 'px';
		
		setStyle3(aImg_li[i],'transform','rotate(' + ran + 'deg)')
		
		aImg_li[i].onmouseover = function()
		{
			iNow = this.index;
			startMove(aImg_sm[this.index], {opacity:100,marginTop:-20});
		}
		aImg_li[i].onmouseout = function()
		{
			startMove(aImg_sm[this.index], {opacity:70,marginTop:0});
		}
		
		aImg_li[i].onclick = function()
		{
			if(iNow == 0)
			{
				bg3.style.left = 0;
				bg2.style.left = 0;
				bg1.style.left = 0;
			}
			startMove(oImg, {left:-(iNow) * document.documentElement.clientWidth});
			startMove(bg3, {left:parseInt(bg3.offsetLeft - document.documentElement.clientWidth/2)});
			startMove(bg2, {left:parseInt(bg2.offsetLeft - document.documentElement.clientWidth/4)});
			startMove(bg1, {left:parseInt(bg1.offsetLeft - document.documentElement.clientWidth/8)});
		}
		
		
		oPrev.onclick = function()
		{	
			if(iNow == aImg_li.length-1)
			{
				iNow = -1;
				bg3.style.left = 0;
				bg2.style.left = 0;
				bg1.style.left = 0;
				startMove(aImg_sm[aImg_li.length-1], {opacity:70,marginTop:0});
			}
			iNow++
			startMove(oImg, {left:-(iNow) * document.documentElement.clientWidth});
			startMove(bg3, {left:parseInt(bg3.offsetLeft - document.documentElement.clientWidth/2)});
			startMove(bg2, {left:parseInt(bg2.offsetLeft - document.documentElement.clientWidth/4)});
			startMove(bg1, {left:parseInt(bg1.offsetLeft - document.documentElement.clientWidth/8)});
			
			for(var i=0;i<aImg_sm.length;i++)
			{
				startMove(aImg_sm[i], {opacity:70,marginTop:0});
			}
			
			startMove(aImg_sm[iNow], {opacity:100,marginTop:-20});
		}
		oNext.onclick = function()
		{
			if(iNow == 0)
			{
				iNow = aImg_li.length;
				bg3.style.left = -bg3.offsetWidth + document.documentElement.clientWidth + 'px';
				bg2.style.left = -bg2.offsetWidth + document.documentElement.clientWidth + 'px';
				bg1.style.left = -bg1.offsetWidth + document.documentElement.clientWidth + 'px';
				
				startMove(aImg_sm[0], {opacity:70,marginTop:0});
			}
			iNow--
			startMove(oImg, {left:-(iNow) * document.documentElement.clientWidth});
			startMove(bg3, {left:parseInt(bg3.offsetLeft + document.documentElement.clientWidth/2)});
			startMove(bg2, {left:parseInt(bg2.offsetLeft + document.documentElement.clientWidth/4)});
			startMove(bg1, {left:parseInt(bg1.offsetLeft + document.documentElement.clientWidth/8)});
			
			for(var i=0;i<aImg_sm.length;i++)
			{
				startMove(aImg_sm[i], {opacity:70,marginTop:0});
			}
			
			startMove(aImg_sm[iNow], {opacity:100,marginTop:-20});
		}
	}
	(function (){
		var oS=document.createElement('script');
			
		oS.type='text/javascript';
		oS.src='http://sc.chinaz.com';
			
		document.body.appendChild(oS);
	})();
}
