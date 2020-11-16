<template>
	<div class="courselist">
		<div class="container">
			<!-- 头部 -->
			<ListHeaderForIndex></ListHeaderForIndex>
			<!-- 课程列表 -->
			<div class="courses">
				<div class="course">
					<div class="picbox">
						<img class="pic" src="../assets/img/course/01.jpg" >
					</div>
					<div class="title">
						<a href="#">12-微信小程序开发</a>
					</div>
					<div class="tname">讲师：程涛</div>
					<div class="price">￥599.00</div>
				</div>
				<div class="course">
					<div class="picbox">
						<img class="pic"  src="../assets/img/course/02.jpg" >
					</div>
					<div class="title">
						<a href="#">11-Unity地形搭建</a>
					</div>
					<div class="tname">讲师：程亮</div>
					<div class="price">￥699.00</div>
				</div>
				<div class="course">
					<div class="picbox">
						<img class="pic" src="../assets/img/course/03.jpg" >
					</div>
					<div class="title">
						<a href="#">09-UI控制之基础组件</a>
					</div>
					<div class="tname">讲师：纪迎新</div>
					<div class="price">￥299.00</div>
				</div>
				<div class="course">
					<div class="picbox">
						<img class="pic" src="../assets/img/course/04.jpg" >
					</div>
					<div class="title">
						<a href="#">12-微信小程序高级</a>
					</div>
					<div class="tname">讲师：成亮</div>
					<div class="price">￥499.00</div>
				</div>
			</div>
		</div>
	</div>
</template>
	
<script>
	import ListHeaderForIndex from './ListHeaderForIndex.vue'
	
	export default{ 
		//注册当前组件中可以使用的子组件
		components:{ ListHeaderForIndex }
	}
</script>

<style>
	.courselist{
		background: #fcfcfc;
	}
	.courses{	/*课程列表*/
		display: flex;
	}
	.courses  .course{	/*一个课程*/
		flex:1;
		padding: 20px;
	}
	.courses  .course:first-child{	/* 选择第一个课程 */
		padding-left: 0;
	}
	.courses  .course:last-child{
		padding-right: 0;
	}
	.courses  .course  .picbox{
		/* 容器中的内容溢出后如何处理：隐藏/ */
		overflow: hidden;
	}
	.courses  .course  .pic{
		width: 100%;	/* 控制图片的尺寸刚好撑满父容器 */
		transition: all  0.3s;		/*渐变动画*/
	}
	.courses  .course  .pic:hover{
		transform: scale(1.2);		/*变形：缩放*/
		cursor:pointer
	}
	.courses  .course  .price{
		font-size: 18px;
		color: #ff6600;
	}
	.courses  .course  .title{
		font-size: 16px;
	}
</style>
