<template>
<div id="home">
	<div class="top">
		<img src="../../static/images/home-top.jpg">
	</div>
	<img class="middle" src="../../static/images/home-middle.svg">
	<div class="bottom">
		<img src="../../static/images/home-bottom.jpg">
	</div>
	<router-link to="/ui_list.html">	
		<img class="arrow" src="../../static/images/home-arrow.svg">
	</router-link>
</div>
</template>

<script>
    export default {
        name: "Home"
    }
</script>

<style scoped>
	#home{
	position:relative;
	height:100vh;
}
.top{
	position:absolute;
	top:10%;
	left:10%;
	width:80%;
	height:30%;
	overflow:hidden;
}
.top img{
	width:100%;
	animation:topMove 2s;
	position:absolute;
}
.bottom img{
	width:100%;
	position:absolute;
	animation:bottomMove 2s;
}
.middle{
	position:absolute;
	right:0;
	left:0;
	top:40%;
	margin:auto;
	animation:middleMove 2s;
	animation-fill-mode:forwards;
}
.bottom{
	position:absolute;
	top:70%;
	right:10%;
	width:80%;
	height:15%;
	overflow:hidden;
}
.arrow{
	position:absolute;
	width:60px;
	left:calc(50% - 30px);
	bottom:20px;
}
@keyframes middleMove{
	form {top:40%}
	to {top:54%}
}
@keyframes topMove{
	from {left:-100%}
	to {left:0}
}
@keyframes bottomMove{
	from {right:-100%}
	to	{right:0}
}
</style>
