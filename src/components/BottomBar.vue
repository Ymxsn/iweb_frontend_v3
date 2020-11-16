<template>
	<div class="bottombar">
		<div class="container">
			<!-- 服务列表 -->
			<div class="servicelist">
				<div class="services">
					<div class="service">
						<h3>关于i前端</h3>
						<ul>
							<li><a href="#">发展历程</a></li>
							<li><a href="#">管理团队</a></li>
							<li><a href="#">企业文化</a></li>
							<li><a href="#">加入我们</a></li>
						</ul>
					</div>
					<div class="service">
						<h3>新手帮助</h3>
						<ul>
							<li><a href="#">学员账号</a></li>
							<li><a href="#">选课流程</a></li>
							<li><a href="#">网报流程</a></li>
							<li><a href="#">上课地点</a></li>
						</ul>
					</div>
					<div class="service">
						<h3>常见问题</h3>
						<ul>
							<li><a href="#">如何注册</a></li>
							<li><a href="#">如何搜课</a></li>
							<li><a href="#">如何报名</a></li>
							<li><a href="#">如何缴费</a></li>
						</ul>
					</div>
					<div class="service">
						<h3>联系我们</h3>
						<ul>
							<li><a href="#">校区电话</a></li>
							<li><a href="#">意见建议</a></li>
							<li><a href="#">联系邮箱</a></li>
						</ul>
					</div>
				</div>
				<div class="hotline">
					<div class="left">	<!-- left宽高为100，而电话图标只有40px -->
						<span class="phone"></span>		<!-- 使用span显示图片，而不是left -->
					</div>
					<div class="right">
						<div>客服热线</div>
						<div>4008-220-220（9:00-24:00）</div>
					</div>
				</div>
			</div>
			<!-- 版权声明 -->
			<div class="copyright">
				<div>Copyright © 2016 iqianduan.com, All Rights Reserved 版权所有</div>
				<div>北京前端教育科技有限公司　京ICP备123456号-1 京公网安备110180201608号</div>
			</div>
		</div>
	</div>
</template>

<script>
</script>

<style>
	.bottombar{
		background: #eee;
		border-top: 1px solid #ddd;
	}
	.servicelist{		/*弹性父容器*/
		display: flex;
	}
	.servicelist  .services{	/*弹性子元素，同时也是一个弹性父容器*/
		flex:615;
		display: flex;
	}
	.servicelist  .services  .service{
		flex:1;
	}
	.servicelist  .hotline{		/*弹性子元素，同时也是一个弹性父容器*/
		flex:385;
		display: flex;
	}
	.servicelist  .hotline  .left{
		flex:100;
		padding: 40px  0  0  50px;	/*上右下左*/
	}
	.servicelist  .hotline  .left  .phone{
		display: inline-block;
		width: 40px;
		height: 40px;
		background-image: url(../assets/img/iconlist.png);
		background-position: 0 -410px;
	}
	.servicelist  .hotline  .right{
		flex:285;
		padding: 40px  0  0  0;
		font-size: 1.3em;
	}
	.copyright{
		text-align: center;
		color: #999;
		padding: 8px 0;
		border-top: 1px solid #ddd;
		line-height: 20px;
	}
</style>
