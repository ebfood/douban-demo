<template>
	<view>
		<view class="banner">
			<image class="banner1" src="../../static/bangdan_banner1.png" mode="aspectFit"></image>
			<image class="banner2" src="../../static/bangdan_banner2.png" mode="aspectFit"></image>
		</view>
		
		<view class="categories">
			<list-category v-for="n of 10" :key="n"></list-category>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.banner {
		width: 100%;
		padding: 10rpx;
		box-sizing: border-box;

		image {
			width: 730rpx;
			height: 350rpx;
			border-radius: 30rpx;
		}
	}
	
	.categories {
		width: 100%;
		padding: 10rpx;
		box-sizing: border-box;
	}
</style>
