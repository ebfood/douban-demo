<template>
	<view class="comment">
		<input type="text" placeholder="说点什么吧..." />
		<button type="default">发送</button>
	</view>
</template>

<script>
	export default {
		name: "comment",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.comment {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 750rpx;
		height: 150rpx;
		background-color: #fff;

		input {
			display: inline-block;
			flex: 1;
			background-color: #eee;
			height: 100rpx;
			margin: 0 20rpx;
			padding: 0 20rpx;
			border-radius: 20rpx;
			border: 2rpx solid $uni-border-color;
		}

		button {
			background-color: $base-color;
			color: #fff;
			width: 150rpx;
			height: 100rpx;
			margin-right: 20rpx;
		}
	}
</style>
