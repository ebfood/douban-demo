<template>
	<view class="detail-board">
		<view class="cover">
			<image src="../../static/p2635676317.jpg" mode="scaleToFill"></image>
		</view>
		<view class="text">
			<h2>六人-泰坦尼克上的中国幸存者</h2>
			<h3>The Six (2020)</h3>
			<text>中国大陆 / 纪录片 /  片长102分钟</text>
			
			<view class="buttons">
				<button type="default">想看</button>
				<button type="default">看过</button>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"detail-board",
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
.detail-board {
	display: flex;
	align-items: center;
	margin: 20rpx auto;
	
	.cover {
		width: 250rpx;
		height: 350rpx;
		overflow: hidden;
		background-color: red;
		margin: 20rpx;
		border-radius: $uni-border-radius-lg;
		@include bgImg(250rpx, 350rpx, "~@/static/logo.png");
		
		image {
			width: 100%;
			height: 100%;
		}
	}
	
	.text {
		flex: 1;
		padding: 0 10rpx;
		
		h2 {
			font-weight: bold;
			font-size: 48rpx;
		}
		
		h3, text {
			color: $uni-text-color-grey;
			font-weight: normal;
		}
		
		text {
			font-size: 28rpx;
		}
		
		.buttons {
			display: flex;
			margin-top: 10rpx;
			button {
				width: 200rpx;
				font-weight: bold;
			}
		}
	}
}
</style>
