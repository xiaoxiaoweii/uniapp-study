<template>
	<view class="content">
		<view class="box2" hover-class="box2-active">
			<view class="box" hover-class="box-active" hover-stop-propagation :hover-start-time="2000" :hover-stay-time="2000">
				我是一个大盒子
			</view>
		</view>
		<image src="../../static/logo.png" mode=""></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '联系我们'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.box {
		width: 100px;
		height: 100px;
		background: #4CD964;
	}
	.box2 {
		width: 200px;
		height: 200px;
		background: #007AFF;
	}
	.box2-active {
		width: 200px;
		height: 200px;
		background: #DD524D;
	}
	.box-active {
		width: 120px;
		height: 120px;
		background: #DD524D;
	}
</style>
