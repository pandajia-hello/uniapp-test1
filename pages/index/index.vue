<template>
	<view class="container">
		<view :style="{height: viewHeight}">
			<scroll-view class="scroll" scroll-y="true" @scrolltolower="handleLower">
				<view v-for="item in 100" style="height: 200rpx;">{{ item }}</view>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				viewHeight: 0
			}
		},
		methods: {
			handleLower() {
				uni.showToast({
					title: '到底了',
					icon: 'none'
				})
			}
		},
		onShow() {
			
		},
		onLoad(options) {
			uni.showToast({
				
			})
			this.viewHeight = uni.getSystemInfoSync().windowHeight + 'px'
		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
	.scroll{
		height: 100%;
		background-color: skyblue;
	}
</style>
