<template>
	<!-- 3楼：导航条 -->
	<div class="navbar">
		<div class="container">
			<!-- 左侧的功能列表 -->
			<ul class="menu">
				<li class="active"><a href="index.html">首页</a></li>
				<li><a href="course.html">全部课程</a></li>
				<li><a href="course.html?tid=1">基础课程</a></li>
				<li><a href="course.html?tid=2">核心课程</a></li>
				<li><a href="course.html?tid=3">进阶课程</a></li>
				<li><a href="teacher.html">名师堂</a></li>
				<li><a href="school.html">校区</a></li>
			</ul>
			<!-- 右侧的登录/注册菜单 -->
			<div class="login-register-box">
				<a href="#">登录</a>
				<span>|</span>
				<a href="#">注册</a>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		
	}
</script>

<style>
	.navbar {
		background: #57BC4C;
		width: 100%;
		height: 42px;
		border-bottom: 2px solid #c1eebd;
		line-height: 39px;
		color: #fff;
		font-size: 1.2em;
	}
	.navbar  .menu {
		
	}
	.navbar  .menu  li {
		float: left;	/*让原本的块级元素li全部浮动起来*/
		padding: 0  1.5em;
	}
	.navbar  .menu  li.active {
		background: #3da232;
	}
	.navbar  .menu  li:hover {
		background: #4AAF3F;
	}
	.navbar  .menu  li  a {		/*使用复杂选择器具有更高的优先级*/
		color: #fff;
	}
	.navbar  .login-register-box {
		float: right;
		background: #77c558;
		padding: 0  2em;
	}
	.navbar  .login-register-box  a {
		color: #fff;
	}
	.navbar  .login-register-box  a:hover {
		color: #FBFC95;
	}
	.navbar  .login-register-box  span {
		margin: 0  0.5em;
	}
</style>
