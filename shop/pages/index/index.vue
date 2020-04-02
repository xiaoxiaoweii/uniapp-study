<template>
	<view>
		首页
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
				console.log('获取轮播图的数据')
				uni.request({
					url: '../../static/api/luobotu.json',
					method: 'get',
					success: res => {
						console.log(res)
						// 如果data下的status不为0 返回 给提示
						if(res.data.status !==0){
							// 提示
							return uni.showToast({
								title:'获取数据失败'
							})
						}
						this.swipers = res.data.message
					}
				})
			}
		}
	}
</script>

<style>
	
</style>
