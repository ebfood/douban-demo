<template>
	<view class="description">
		<view class="title"> 简介 </view>
		<text :style="{ '-webkit-line-clamp': displayLine }">{{description}}</text>
		<view class="expand" @click="handleExpand" v-if="expand">展开</view>
		<view class="expand" @click="handleShrank" v-if="!expand">收起</view>
	</view>
</template>

<script>
	export default {
		name: "detail-description",
		data() {
			return {
				expand: true,
				displayLine: 5,
				description: "description: '1912年4月14日泰坦尼克号沉没后几乎所有幸存者被送回至纽约港口，唯独六名中国幸存者，他们获救后在24小时之内被美国驱逐出境，他们的逃生经历几乎不被记录，甚至被刻意抹去。本片由詹姆斯·卡梅隆监制，我们将跟随调查者，追寻这六人从人类史上最大海难中死里逃生的经历和人生轨迹，拆穿被掩盖一个世纪之久的谎言。'"
			};
		},
		methods:{
			handleExpand() {
				this.expand = false //隐藏显示
				this.displayLine = 10
			},
			handleShrank() {
				this.expand = true //隐藏显示
				this.displayLine = 5
			}
		}
	}
</script>

<style lang="scss">
	.description {
		padding: 0 40rpx;

		.title {
			font-size: 36rpx;
			font-weight: bold;
			margin-bottom: 20rpx;
		}

		text {
			text-indent: 20rpx;
			overflow: hidden;
			text-overflow: ellipsis;
			display: -webkit-box;
			-webkit-line-clamp: 5;
			/* 多行文本的行数  3 - 表示三行文本超出后在第三行后显示（...） */
			-webkit-box-orient: vertical;
			/* 比较适用于webkit浏览器及移动端浏览器（不兼容） */
		}

		.expand {
			color: $base-color;
			float: right;
		}
	}
</style>
