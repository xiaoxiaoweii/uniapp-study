<template>
	<view class="home">
		<swiper indicator-dots circular>
			<swiper-item v-for="item in swipers" :key="item.id">
				<image :src="item.img"></image>
			</swiper-item>
		</swiper>
		<!-- 导航区域 -->
		<view class="nav">
			<view class="nav_item">
				<view class="">
					
				</view>
				<text>黑马超市</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swipers: []
			}
		},
		onLoad() {
			// 页面加载 获取轮播图数据
			this.getSwiper()
		},
		methods: {
			// 获取轮播图的数据
			getSwiper () {
				console.log('获取轮播图数据')
				uni.request({
					url:'../../static/api/lunbotu.json',
					success: res=> {
						console.log(res)
						if(res.data.status !==0){
							return uni.showToast({
								title:'获取数据失败',
								icon: 'none'
							})
						}
						this.swipers = res.data.message
					}
				})
			}
		}
	}
</script>

<style lang="scss">
	.home {
		swiper{
			width: 750rpx;
			height: 380rpx;
			image{
				height: 100%;
				width: 100%;
			}
		}
	}
</style>
