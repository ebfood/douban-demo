<template>
	<view class="content">
		<view class="search-container">
			<view class="search">
				<uni-search-bar :radius="10" @confirm="search" placeholder="搜索"></uni-search-bar>
			</view>
		</view>

		<!-- 内容块 -->
		<view class="content-block" v-for="(block, index) in indexArray" :key="index">
			<!-- 标题栏 -->
			<block-title :text="block.title" :url="'#'"></block-title>
			<!-- 滚动栏 -->
			<scroll-view scroll-x="true" @scroll="scroll">
				<view class="scroll-view_H">
					<film v-for="(film,ind) in block.films" :key="ind" :src="film.coverSrc" :title="film.title" :score="film.score"></film>
				</view>
			</scroll-view>
		</view>

	</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '院线热映',
				src: '../../static/p2635676317.jpg',
				indexArray: [{
					title: '院线热映',
					films: [{
							coverSrc: '../../static/p2635676317.jpg',
							title: '六人-泰坦尼克上的中国幸存者',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2635676317.jpg',
							title: '六人-泰坦尼克上的中国幸存者',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2635676317.jpg',
							title: '六人-泰坦尼克上的中国幸存者',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2635676317.jpg',
							title: '六人-泰坦尼克上的中国幸存者',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2635676317.jpg',
							title: '六人-泰坦尼克上的中国幸存者',
							score: Math.floor((Math.random()*3+7)*10)/10
						}
					]
				},
				{
					title: '豆瓣热门',
					films: [
						{
							coverSrc: '../../static/p2633966702.jpg',
							title: '小人物',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2633966702.jpg',
							title: '小人物',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2633966702.jpg',
							title: '小人物',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2633966702.jpg',
							title: '小人物',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2633966702.jpg',
							title: '小人物',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
					]
				},
				{
					title: '近期热门剧集',
					films: [
						{
							coverSrc: '../../static/p2631873666.jpg',
							title: '觉醒年代',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2631873666.jpg',
							title: '觉醒年代',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2631873666.jpg',
							title: '觉醒年代',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2631873666.jpg',
							title: '觉醒年代',
							score: Math.floor((Math.random()*3+7)*10)/10
						},
						{
							coverSrc: '../../static/p2631873666.jpg',
							title: '觉醒年代',
							score: Math.floor((Math.random()*3+7)*10)/10
						}
					]
				}]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.search-container {
		width: 750rpx;
		height: 104rpx;
		
	}
	
	.search {
		width: 750rpx;
		background-color: $base-color;
		position: fixed;
		top: var(--window-top);
		left: 0;
		z-index: 10;
	}
	

	.content-block {
		.scroll-view_H {
			display: flex;
			flex-wrap: nowrap;
		}
	}
</style>
