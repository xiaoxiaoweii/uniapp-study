<template>
	<view>
		<view class="news_item" v-for="(item, index) in newsData" :key="index" @click="navigator">
			<image :src="item.url"></image>
			<view class="right">
				<view class="tit">
					{{item.title}}
				</view>
				<view class="info">
			        <text>发表时间:{{item.time}}</text>
					<text>浏览:{{item.see}}</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: ["newsData"],
		data() {
			return {
				
			}
		},
		methods: {
			navigator() {
				this.$emit('itemClick')
			}
		}
	}
</script>

<style lang="scss">
	.news_item{
		display: flex;
		padding: 10rpx 20rpx;
		border-bottom: 1px solid $shop-color;
		image{
			width: 200rpx;
			height: 150rpx;
		}
		.right{
			margin-left: 15rpx;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			.tit{
				font-size: 30rpx;
			}
			.info{
				font-size: 24rpx;
				text:nth-child(2){
					margin-left: 30rpx;
				}
			}
		}
		
	}
</style>
