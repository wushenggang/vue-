<template>
<div id="paint">
	<div class="text-box">
		<p class="title">PAINTS</p>
		<p class="desc">这些东西决定了作品的高度<br>触类旁通，个人平日的积累，练习有很大的意义</p>
	</div>
	<div id="jswbox">
    <pre class="prev">prev</pre>
    <pre class="next">next</pre>
    <ul>
        <li><img src="../../static/images/paint1.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint2.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint3.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint4.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint5.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint6.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint7.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint8.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint9.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint10.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint11.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
        <li><img src="../../static/images/paint12.jpg" />
        	<p class="inner-title">绘画练习</p>
        	<p class="date">February 2018</p>
        </li>
    </ul>
</div>
	<div class="footer">
    <p class="footer-text">
      © made by wushenggang
    </p>
  </div>
</div>
</template>

<script>
    export default {
        name: "Paint",
        mounted(){
        this.$nextTick(function(){
    		$(function(){
    			new ZoomPic("jswbox");
    			})  
    		})
    	}
    }
</script>

<style scoped>
.text-box{
	position:absolute;
	top:20%;
	left:17%;
}
.text-box .title{
	float:left;
	padding-left:0px;
	animation:textMove 1s;
	writing-mode:tb-rl;
	opacity:1;
	font-size:60px;
	display:block;
	font-family:customFont;
	text-align:left;
	color:#000000;
}
.text-box .desc{
	letter-spacing:7px;
	padding-left:35px;
	float:left;
	writing-mode:tb-rl;
	opacity:1;
	font-size:16px;
}
li{
	background:#fff;
	text-align:center;
	box-shadow:0 0 20px rgba(0,0,0,0.1);
}
li img{
	padding-top:4%;
	max-width:100%;
	max-height:70%;
}
.inner-title{
	position:absolute;
	bottom:5.5vh;
	width:100%;
	text-align:center;
	font-size:20px;
	font-family:customFont;
	letter-spacing:1px;
}
.date{
	position:absolute;
	bottom:2vh;
	width:100%;
	text-align:center;
	font-size:12px;
	font-family:customFont;
	opacity:0.5;
}
@keyframes textMove{
	from {padding-left:60px}
	to	{padding-left:0px}
}
.footer{
    margin-top: 80px;
    width: calc(100vw - 160px);
    height: 50px;
    background: #1f2021;
    position:absolute;
    bottom:0;
  }
  .footer-text{
    bottom: 0;
    width: 100%;
    color: #fff;
    text-align: center;
    font-size: 14px;
    line-height: 50px;
    opacity: 0.6;
  }
</style>
