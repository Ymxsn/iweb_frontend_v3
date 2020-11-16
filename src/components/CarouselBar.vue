<template>
	<div class="carouselbar">
		<div class="container">
			<div class="carousel">
				<!-- 轮播广告内容1： N张图片 -->
				<img class="item active" src="../assets/img/banner01.jpg" alt="广告0">
				<img class="item" src="../assets/img/banner02.jpg" alt="广告1">
				<img class="item" src="../assets/img/banner03.jpg" alt="广告2">
				<img class="item" src="../assets/img/banner04.jpg" alt="广告3">
				<!-- 轮播广告内容2： 上/下一张轮播控制器 -->
				<div class="control  left">
					<span class="fa fa-chevron-left fa-4x"></span>
				</div>
				<div class="control  right">
					<span class="fa fa-chevron-right fa-4x"></span>
				</div>
				<!-- 轮播广告内容3： 轮播序号指示器 -->
				<ul class="indicators">
					<li class="active"></li>
					<li></li>
					<li></li>
					<li></li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
	export default { }
</script>

<style>
	.carouselbar {
		height: 383px;
		border-bottom: 3px solid #ddd;
	}
	.carousel {				/*轮播广告容器，内部包含轮播控制器*/
		height: 380px;
		position: relative;  /*为绝对定位的子元素提供参照物*/
	}
	.carousel  .item {
		position: absolute;
		top: 0;
		left: 50%;	/*先往右移到父容器的中线处，此处的50%指参照物(父容器)的宽度*/
		height: 380px;
		/* CSS中的变形函数：旋转/缩放/扭曲/平移 */
		transform: translateX(-50%);  /*当前元素向左平移，此处的50%指自己的宽度*/
		z-index: -2;	/*图片降低z轴出现顺序，以露出上面的内容*/
	}
	.carousel  .item.active  {
		z-index: -1;
	}
	.carousel  .control {
		width: 43px;
		height: 75px;
		/*background: rgba(0,0,0, 0.3);  Alpha: 不透明度  —— 仅让背景透明*/
		background: #000;
		opacity: 0.2;					/*背景以及内容都透明*/
		text-align: center;
	}
	.carousel  .control:hover {
		/* background: rgba(0,0,0, 0.6); */
		opacity: 0.6;
	}
	.carousel  .control  .fa {
		line-height: 75px;
		color: #fff;
	}
	.carousel  .control.left {
		float: left;
		margin-left: 12px;
		margin-top: 152.5px;
	}
	.carousel  .control.right {
		float: right;
		margin-right: 12px;
		margin-top: 152.5px;
	}
	.carousel  .indicators {
		/* 此处调整ul的位置可以使用margin或者绝对定位 */
		position: absolute;
		bottom: 20px;
		left: 50%;
		transform: translateX(-50%);
	}
	.carousel  .indicators  li{
		width: 14px;
		height: 14px;
		background: #ccc;
		/* 添加边框圆角半径 */
		border-radius: 50%;
		float: left;
		margin: 0  5px;
		cursor: pointer;   /*光标：指向符*/
	}
	.carousel  .indicators  li.active {
		background: #f90;
	}
</style>
