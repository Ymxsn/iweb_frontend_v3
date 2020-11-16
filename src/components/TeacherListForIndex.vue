<template>
	<div class="teacherlist">
		<div class="container">
			<!-- 列表头 -->
			<ListHeaderForIndex> </ListHeaderForIndex>
			<!-- 讲师列表 -->
			<div class="teachers">
				<div class="teacher">
					<img src="../assets/img/teacher/cl.jpg" class="pic">
					<div class="tname">讲师：成亮</div>
					<div class="maincourse">主讲：WEB全栈开发</div>
				</div>
				<div class="teacher">
					<img src="../assets/img/teacher/ct.jpg" alt="" class="pic">
					<div class="tname">讲师：程涛</div>
					<div class="maincourse">主讲：移动APP开发</div>
				</div>
				<div class="teacher">
					<img src="../assets/img/teacher/jyx.jpg" alt="" class="pic">
					<div class="tname">讲师：纪迎新</div>
					<div class="maincourse">主讲：前段框架开发</div>
				</div>
				<div class="teacher">
					<img src="../assets/img/teacher/zd.jpg" alt="" class="pic">
					<div class="tname">讲师：张东</div>
					<div class="maincourse">主讲：JS高级编程</div>
				</div>
				<div class="teacher">
					<img src="../assets/img/teacher/lr.jpg" alt="" class="pic">
					<div class="tname">讲师：李然</div>
					<div class="maincourse">主讲：高级网页设计</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import ListHeaderForIndex from './ListHeaderForIndex.vue'
	export default {
		components:{ListHeaderForIndex}
	}
</script>

<style>
	.teacherlist{
		background: #fcfcfc;
	}
	.teachers{	/*弹性父容器*/
		display: flex;
	}
	.teachers  .teacher{	/*弹性子元素*/
		flex:1;
		padding: 20px 12.5px 40px;
	}
	.teachers  .teacher:first-child{	/*第一个讲师*/
		padding-left:0 ;
	}
	.teachers  .teacher:last-child{	/*第一个讲师*/
		padding-right:0 ;
	}
	.teachers  .teacher  .pic{
		width: 100%; /*图片的宽就是父容的宽器*/
	}
	.teachers  .teacher  .tname{
		text-align: center;
	}
	.teachers  .teacher  .maincourse{
		text-align: center;
		font-size: .8em;
		color: #999;
	}
</style>
