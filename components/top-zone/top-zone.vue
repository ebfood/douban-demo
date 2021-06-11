<template>
	<view>
		<view class="status_bar" ref="statusbar">
			<!-- 这里是状态栏 -->
		</view>

		<view>
			<uni-nav-bar left-icon="back" left-text="返回" title="电影详情" backgroundColor="#42bd56" color="#fff">
			</uni-nav-bar>
		</view>
	</view>
</template>

<script>
	export default {
		name: "top-zone",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.status_bar {
		height: var(--status-bar-height);
		width: 100%;
		background-color: $base-color;
	}

</style>
