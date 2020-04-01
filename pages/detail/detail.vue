<template>
	<view class="content">
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<view class="text-area">
			<text class="title" selectable>{{title}}</text>
		</view>
		<view class="text-area">
			<text class="title" selectable space="ensp">唱歌   跳舞 篮球</text>
		</view>
		<view class="text-area">
			<text class="title" selectable space="ensp" decode="">唱歌   跳舞 篮球&nbsp;</text>
		</view>
		<button type="default">按钮</button>
		<button type="default" size="mini">按钮</button>
		<button type="warn" size="mini">按钮</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '唱歌跳舞篮球'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
