<template>
	<view class="list-category">
		<view class="cover"></view>
		<view class="text">
			<view class="top">
				<view v-for="(item, index) in tops" :key="item.title">{{index+1 + '. ' + item.title}}<text>{{item.score}}分</text></view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"list-category",
		data() {
			return {
				tops: [
					{
						title: '肖申克的救赎',
						score: 9.7
					},
					{
						title: '霸王别姬',
						score: 9.6
					},
					{
						title: '阿甘正传',
						score: 9.5
					}
				]
			};
		}
	}
</script>

<style lang="scss">
.list-category {
	display: flex;
	justify-content: center;
	align-items: center;
	margin-bottom: 30rpx;
	
	.cover {
		width: 250rpx;
		height: 250rpx;
		background-color: red;
		border-radius: 20rpx;
		@include bgImg(250rpx, 250rpx, "../../static/bangdan_cover1.png");
	}
	
	.text {
		flex: 1;
		padding: 30rpx;
		font-size: 28rpx;
		border: 1px solid $uni-border-color;
		border-left: none;
		border-radius: 0 $uni-border-radius-lg $uni-border-radius-lg 0;
		
		.top {
			font-size: 36rpx;
			color: #666;
			
			text {
				margin-left: 20rpx;
				color: #ffae33;
				font-size: 32rpx;
				line-height: 60rpx;
			}
		}
	}
}
</style>
