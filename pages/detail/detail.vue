<template>
	<view class="detail">
		<top-zone></top-zone>

		<view class="toptab" @click="handleTab($event)">
			<view v-for="(item, index) in tabData" :key="index" :id="index" class="tabs"
				:class="{selected:currTab == index}">
				{{item}}
			</view>
		</view>

		<view class="scroll" v-if="currTab==0">
			<scroll-view class="content" scroll-y="true">
				<detail-board></detail-board>
				<detail-description  v-for="(item, index) of 10" :key="index"></detail-description>
			</scroll-view>
		</view>

		<view class="subtab" v-if="currTab==1">xxxx</view>
		<view class="subtab" v-if="currTab==2">yyyy</view>

		<comment></comment>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				tabData: ['简介', '详情', '评论'],
				currTab: '0'
			};
		},
		methods: {
			handleTab(e) {
				if (e.target.id)
					this.currTab = e.target.id
			}
		}
	}
</script>

<style lang="scss">
	/* */
	page {
		background-color: #f4f6f9;
		height: 100%;
	}

	.detail {
		height: 100%;
		display: flex;
		flex-direction: column;


		.scroll {
			flex: 1;
			overflow: hidden;  // BFC

			.content {
				height: 100%;
			}
		}

		.toptab {
			display: flex;
			justify-content: center;
			align-items: center;
			width: 100%;
			height: 60rpx;

			.tabs {
				box-sizing: content-box;
				padding: 0 50rpx; //撑开
				font-weight: bold;
				color: #999999;
				text-align: center;
				border-bottom: 4rpx solid rgba($color: #000000, $alpha: 0);
			}

			.selected {
				border-bottom: 4rpx solid $base-color;
			}
		}

		.subtab {
			flex: 1;
		}
	}
</style>
