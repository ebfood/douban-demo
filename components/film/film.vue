<template>
	<navigator class="film" url="../../pages/detail/detail?id=000001">
		<image :src="src" class="cover" lazy-load></image>
		<view class="title">{{title}}</view>
		<view class="score">
			<view class="stars">
				<uni-rate :size="16" :value="score/2" :is-fill="false" :readonly="true" />
			</view>
			<view class="value">{{score}}</view>
		</view>
	</navigator>
</template>

<script>
	export default {
		name: "film",
		props: ['src', 'title', 'score'],
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.film {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 250rpx;


		.score {
			display: flex;
			// justify-content: center;
			align-content: center;
			height: 30rpx;
			width: 90%;
			padding: 10rpx;

			.stars {
				display: flex;
				align-items: center;
				margin: 6rpx;
			}

			.value {
				font-size: 32rpx;
				color: $uni-text-color-grey;
			}
		}

		.cover {
			width: 200rpx;
			height: 280rpx;
			border-radius: 10rpx;
		}

		.title {
			box-sizing: border-box;
			width: 90%;
			padding: 10rpx;
			overflow: hidden;
			text-overflow: ellipsis;
			white-space: nowrap;
			font-weight: bold;
			font-size: 36rpx;
			text-align: center;
		}
	}
</style>
