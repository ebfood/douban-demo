<template>
	<view class="block-title">
		<text class="text">{{ text }}</text>
		<navigator class="more" :url="url">查看更多></navigator>
	</view>
</template>

<script>
	export default {
		name:"block-title",
		props: ['text', 'url'],
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
.block-title {
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 20rpx;
	height: 50rpx;
	
	.text {
		font-weight: bold;
		color: $uni-text-color;
	}
	
	.more {
		color: $base-color;
	}
}
</style>
