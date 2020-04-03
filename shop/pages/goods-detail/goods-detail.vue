<template>
	<view class="home">
		<swiper indicator-dots circular>
			<swiper-item v-for="item in swipers" :key="item.id" @click="navigator">
				<!-- <image :src="item.img"></image> -->
				<image :src="item.img" mode=""></image>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				// 轮播图数据
				swipers: [{
						"id": 1,
						"url": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/91538/35/1275/99931/5dbbf626Ed9e6f56c/6f5681b0d1362012.jpg!cr_1125x445_0_171!q70.jpg",
						"img": "http://m.360buyimg.com/mobilecms/s750x750_jfs/t1/51796/3/3090/165250/5d0da795Eab1d07e8/780a99bc93e0230b.png!q80.dpg.webp"
					},
					{
						"id": 2,
						"url": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/98983/25/16598/202926/5e7da468E23a636f6/ae88aa976df65991.jpg!cr_1125x445_0_171!q70.jpg",
						"img": "http://m.360buyimg.com/mobilecms/s720x720_jfs/t1/45374/19/3033/67880/5d0da7ceEfd0c60dd/bf4c0964c6f7ddbc.jpg!q70.dpg.webp"
					},
					{
						"id": 3,
						"url": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg",
						"img": "http://m.360buyimg.com/mobilecms/s720x720_jfs/t1/73783/6/2649/42548/5d0da7ceEc1418ad8/97fa482269cf7175.jpg!q70.dpg.webp"
					}
				],
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	// 轮播图
	.home {
		swiper{
			width: 750rpx;
			height: 700rpx;
			image {
				height: 100%;
				width: 100%;
			}
		}
	}
</style>
