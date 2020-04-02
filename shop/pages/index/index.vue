<template>
	<view class="home">
		<swiper indicator-dots circular>
			<swiper-item v-for="item in swipers" :key="item.id">
				<!-- <image :src="item.img"></image> -->
				<image :src="item.img" mode=""></image>
			</swiper-item>
		</swiper>
		<!-- 导航区域 -->
		<view class="nav">
			<view class="nav_item" v-for="(item, index) in navs_1" :key="index" @click="navItemClick(item.path)">
				<view :class="item.icon"></view>
				<text>{{item.title}}</text>
			</view>
		</view>
		<view class="nav">
			<view class="nav_item" v-for="(item, index) in navs_2" :key="index" @click="navItemClick(item.path)">
				<view :class="item.icon"></view>
				<text>{{item.title}}</text>
			</view>
		</view>
		<!-- 推荐商品 -->
		<view class="hot_goods">
			<view class="tit">
				推荐商品
			</view>
			<goods-list :goods="goods"></goods-list>
		</view>
	</view>
</template>

<script>
	import goodsList from '../../components/goods-list/goods-list.vue'
	export default {
		data() {
			return {
				// 轮播图数据
				swipers: [{
						"id": 1,
						"url": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/91538/35/1275/99931/5dbbf626Ed9e6f56c/6f5681b0d1362012.jpg!cr_1125x445_0_171!q70.jpg",
						"img": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/91538/35/1275/99931/5dbbf626Ed9e6f56c/6f5681b0d1362012.jpg!cr_1125x445_0_171!q70.jpg"
					},
					{
						"id": 2,
						"url": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/98983/25/16598/202926/5e7da468E23a636f6/ae88aa976df65991.jpg!cr_1125x445_0_171!q70.jpg",
						"img": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/98983/25/16598/202926/5e7da468E23a636f6/ae88aa976df65991.jpg!cr_1125x445_0_171!q70.jpg"
					},
					{
						"id": 3,
						"url": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg",
						"img": "http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg"
					}
				],
				// 推荐商品
				goods: [
					{
					"id": 1,
					"zhaiyao": '美的(Midea)638升 对开门冰箱 抗菌保鲜 智能双变频无霜 一级能效 大容量电冰箱 双门 芙蓉金BCD-638WKPZM(E)',
					"price": 4099,
					"url": 'http://img10.360buyimg.com/mobilecms/s372x372_jfs/t1/101174/7/16702/104493/5e7dd4afEf0c63ddf/e0ef740bc5ca4459.jpg'
					},
					{
					"id": 2,
					"zhaiyao": '格莱西（GELAIXI)雪茄柜 恒温 恒湿 进口 雪松实木层架保湿柜子家用 加湿雪茄柜 BX-48L琥珀金',
					"price": 2580,
					"url": 'http:////img13.360buyimg.com/mobilecms/s372x372_jfs/t1/29035/22/12451/92453/5c987aa9E3f939368/46c3b9b101548465.jpg'
					},
					{
					"id": 3,
					"zhaiyao": '雷神(ThundeRobot) TR-C27H144 27英寸1800R曲率144Hz窄边框曲面/快拆底座/电竞吃鸡显示器（HDMI/DP/DVI)',
					"price": 1199,
					"url": '//img13.360buyimg.com/mobilecms/s372x372_jfs/t1/93179/6/12107/183180/5e44e5f0E089a649a/37960924fdae2534.jpg'
					},
					{
					"id": 4,
					"zhaiyao": '海尔（Haier）258升 风冷无霜三门冰箱 中门5℃~-18℃变温 TABT杀菌 3D立体环绕风 BCD-258WDPM',
					"price": 2299,
					"url": 'http:////img12.360buyimg.com/mobilecms/s372x372_jfs/t1/93017/40/17309/94800/5e843d9dE96e6d60c/b87271facc6a1dd3.jpg'
					},
					{
					"id": 5,
					"zhaiyao": '雷柏（Rapoo） N1200 鼠标 有线鼠标 办公鼠标 静音鼠标 对称鼠标 笔记本鼠标 电脑鼠标 黑色 自营',
					"price": 19,
					"url": 'http://img12.360buyimg.com/mobilecms/s372x372_jfs/t1/48224/31/1666/205406/5cf7c17eEe8bf6fc6/f64b2fd03f39afa6.jpg'
					},
					{
					"id": 6,
					"zhaiyao": '顾致  适用于吉利钥匙壳改装帝豪EC715帝豪EC718鹰GX7鹰SC6英伦远景 【劳斯款】左槽3键钥匙壳',
					"price": 4099,
					"url": 'http://img12.360buyimg.com/mobilecms/s372x372_jfs/t1/69516/9/15423/172141/5dcec557Edeafba6f/888195b4e75c8a8e.jpg!q70.dpg.webp'
					},
					{
					"id": 7,
					"zhaiyao": '老北京布鞋男 手工千层底休闲鞋 春夏款透气吸汗黑色中老年爸爸鞋 厚底防滑耐磨 防臭舒适棉布麻底开车鞋 纯布底 40码(下单立减20) ',
					"price": 128,
					"url": 'http://img13.360buyimg.com/mobilecms/s372x372_jfs/t1/92616/7/12845/61755/5e4f761bE81fb8c53/8da0f8d5e65f8128.jpg!q70.dpg.webp'
					},
					{
					"id": 8,
					"zhaiyao": '三只松鼠混合水果罐头312g/罐 方便食品新鲜糖水柠檬黄桃罐头',
					"price": 17.8,
					"url": 'http://img14.360buyimg.com/mobilecms/s372x372_jfs/t1/109776/36/10717/268393/5e81a464Edeffa157/e9bdb31ba7974873.jpg!q70.dpg.webp'
					}
				],
				navs_1: [
					{
					icon:'iconfont icon-tubiaolunkuo-',
					title: '物流查询',
					path: '/pages/goods/goods'
					},
					{
					icon:'iconfont icon-fuwu',
					title: '充值缴费',
					path: '/pages/goods/goods'
					},
					{
					icon:'iconfont icon-coat',
					title: '晓晓服饰',
					path: '/pages/goods/goods'
					},
					{
					icon:'iconfont icon-shengxian_xie',
					title: '晓晓生鲜',
					path: '/pages/goods/goods'
					}
				],
				navs_2: [
					{
					icon:'iconfont icon-quan',
					title: '领券',
					path: '/pages/goods/goods'
					},
					{
					icon:'iconfont icon-zhuanqian',
					title: '赚钱',
					path: '/pages/goods/goods'
					},
					{
					icon:'iconfont icon-weibiaoti2fuzhi03',
					title: '数码电器',
					path: '/pages/goods/goods'
					},
					{
					icon:'iconfont icon-icon-test',
					title: '拍拍二手',
					path: '/pages/goods/goods'
					},
				]
			}
		},
		comments:{
			"goods-list": goodsList
		},
		onLoad() {
			// 页面加载 获取轮播图数据
			// this.getSwiper()
		},
		methods: {
			// 获取轮播图的数据
			getSwiper() {
				console.log('获取轮播图数据')
				uni.request({
					url: '../../static/api/lunbotu.json',
					method: 'GET',
					success: (res) => {
						console.log(res)
						if (res.data.status !== 0) {
							return uni.showToast({
								title: '获取数据失败',
								icon: 'none'
							})
						}
						this.swipers = res.data.message
					}
				})
			},
			// 获取热门商品数据
			// 导航点击处理函数
			navItemClick (url) {
				// console.log(url)
				uni.navigateTo({
					url
				})
			}
		}
	}
</script>

<style lang="scss">
	// 轮播图
	.home {
		swiper {
			width: 750rpx;
			height: 380rpx;

			image {
				height: 100%;
				width: 100%;
			}
		}
	}

	// 导航区域
	.nav {
		display: flex;

		.nav_item {
			width: 25%;
			text-align: center;

			view {
				width: 120rpx;
				height: 120rpx;
				background: $shop-color;
				border-radius: 60rpx;
				margin: 10px auto;
				line-height: 120rpx;
				color: #fff;
				font-size: 55rpx;
			}
		}

		text {
			font-size: 30rpx;
		}
	}

	// 推荐区域
	.hot_goods {
		background: #eee;
		overflow: hidden;
		margin-top: 14px;
		.tit {
			height: 50px;
			line-height: 50px;
			color: $shop-color;
			text-align: center;
			letter-spacing: 20px;
			background: #fff;
			margin: 10rpx 0;
		}
	}
</style>
