<template>
	<!-- 顶部条组件 -->	
	<TopBar></TopBar>
	<!-- 搜索条组件 -->
	<SearchBar></SearchBar>
	<!-- 导航条组件 -->
	<NavBar></NavBar>
	<!-- 轮播广告组件 -->
	<CarouselBar></CarouselBar>
	<!-- 最新课程 -->
	<CourseListForIndex></CourseListForIndex>
	<!-- 热门课程 -->
	<CourseListForIndex></CourseListForIndex>
	<!-- 名师堂 -->
	<TeacherListForIndex></TeacherListForIndex>
	<!-- 底部条 -->
	<BottomBar></BottomBar>
</template>

<script>
	import TopBar from './components/TopBar.vue'
	import SearchBar from './components/SearchBar.vue'
	import NavBar from './components/NavBar.vue'
	import CarouselBar from './components/CarouselBar.vue'
	import CourseListForIndex from './components/CourseListForIndex.vue'
	import TeacherListForIndex from './components/TeacherListForIndex.vue'
	import BottomBar from './components/BottomBar.vue'
	
	export default {
		//注册当前组件的子组件
		components: {TopBar, SearchBar, NavBar, CarouselBar,CourseListForIndex,
		TeacherListForIndex,BottomBar}
	}
</script>

<style>
	/* 此处放置所有组件的公共样式 */
	.container {				/*在屏幕中水平居中的容器*/
		width: 1000px;
		margin-left: auto;
		margin-right: auto;
		border: 1px solid #aaa;	/*仅供测试用*/
	}
	.theme {					/*主题色*/
	}
	.theme-reverse {			/*主题色的反色*/
		color: #f60;	
	}
</style>