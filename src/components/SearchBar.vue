<template>
	<!-- 2楼：搜索条 -->
	<div class="searchbar">
		<div class="container">
			<!-- 1.LOGO -->
			<!-- <img src="img/logo.png" alt="iWeb LOGO"> 无法显示 -->
			<!-- 直接引用法使用图片 -->
			<img src="../assets/img/logo.png" alt="iWeb LOGO1">
			<!-- 数据绑定法使用图片 -->
			<img :src="logo" alt="iWeb LOGO2">
			<!-- 3.我的购物车 -->
			<div class="cart-container" id="myCart">
				<!-- 购物车：z-index要高于“下拉菜单” -->
				<div class="cart" id="cart">
					<span class="fa fa-shopping-cart fa-lg"></span>
					<span>我的购物车(<b>0</b>)</span>
					<span class="fa fa-caret-down caret" id="caret"></span>
				</div>
				<!-- 下拉菜单 -->
				<div class="dropdown" id="dropdown">
					请登录后查看您的购物车
				</div>
			</div>
			<!-- 2.输入框 -->
			<div class="search">
				<input type="text" placeholder="课程搜索"><span class="fa fa-search fa-lg"></span>
			</div>
		</div>
	</div>
</template>

<script>
	//import 导入只能在最外层
	//require 导入可以在最外层，也可以在内层
	export default {
		//注册当前组件的子组件
		components:{ },
		//声明当前组件可以使用的数据变量
		data(){
			return {
				logo: require('../assets/img/logo.png')   //模型变量，在模板中用:引用
			}
		}
	}
</script>

<style>
	.searchbar {
		width: 100%;
		background: #fff;
	}
	.searchbar > .container {
		padding-top: 2em;
		padding-bottom: 2em;
	}
	.search {
		float: right;  /*搜索条右浮动*/
		margin-top: 6px;
	}
	.search > input {
		width: 430px;
		height: 32px;
		border: 1px solid #ccc;
		/* 输入框获得焦点时的外围轮廓线 */
		outline: none;
		padding-left: .6em;		/*CSS中约定：0.8可简写为.8*/
		padding-right: .6em;
		vertical-align: middle; /*行内块元素与同一行中内容竖直对齐*/
	}
	.search > .fa-search {
		background: #57bc4c;
		color: #fff;
		font-size: 2.2em;
		width: 50px;
		height: 32px;
		line-height: 32px;	/*文字竖直方向上居中*/
		text-align: center; /*文字水平方向上居中*/
		vertical-align: middle; /*行内块元素与同一行中内容竖直对齐*/
	}
	.cart-container {
		/* 修改购物车容器的定位方式，为下拉菜单提供定位参照物，但不脱离文档流 */
		position: relative;
		float: right;
		margin-top: 6px;
		margin-left: 20px;
	}
	.cart {			/*购物车下面没有“下拉菜单”时的样式*/
		background: #f9f9f9;
		border: 1px solid #ddd;
		line-height: 30px;
		/* 修改光标的样式 */
		cursor: pointer;
		position: relative; /*只有定位了的元素才能使用z-index*/
		z-index: 1;
	}
	.cart.open {	/*购物车下面有“下拉菜单”时的样式*/
		line-height: 31px;
		background: #fff;
		/*border-bottom-color: #fff;  下边框颜色*/
		border-bottom: none;
	}
	.cart > .fa {			/*购物车+小三角*/
		padding-left: 0.6em;
		padding-right: 0.6em;
		color: #57BC4C;
	}
	.cart > .caret {		/*小三角的动画基础类*/
		transform: rotate(0);
		transition: all  .3s;	/*渐变动画*/
	}
	.cart > .caret-rotate {	/*小三角的动画目标类*/
		transform: rotate(180deg);
	}
	.cart-container > .dropdown {		/*下拉菜单不显示时的样式*/
		position: absolute; /*绝对定位的元素可以处于其他元素上方*/
		top: 31px;
		right: 0;	
		border: 1px solid #ddd;
		/* padding: 2em  3em  2em  3em;   上右下左*/
		/* padding: 2em 3em 2em;  上右下，左和右的值相同 */
		padding: 2em  3em;  /*上右， 下和上相同，左和右相同*/
		width: 262px;
		background: #fff;	/*DIV元素的默认背景色为透明色*/
		display: none;	/* 不显示下拉菜单 */
	}
	.cart-container > .dropdown.open {	/*下拉菜单不显示时的样式*/
		display: block;
	}
</style>
