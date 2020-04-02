<template>
	<view>
		<goods-list :goods="goods"></goods-list>
		<view class="isOver" v-if="flag">
			-----我是有底线的-----
		</view>
	</view>
</template>

<script>
	import goodsList from '../../components/goods-list/goods-list.vue'
	export default {
		data() {
			return {
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
				flag: true
			}
		},
		onReachBottom() {
			console.log('触底')
			// 获取第二页数据 保留第一页
			// 将数据都放在goods中
			// if(this.goods.length < this.pageindex*10) return this.flag = true
		},
		onPullDownRefresh() {
			console.log('下拉刷新')
			const Ngoods = this.goods
			this.goods =[]
			this.flag = false
			setTimeout(()=>{
				uni.stopPullDownRefresh()
				this.goods = Ngoods
				this.flag = true
			}, 1000)	
		},
		components: {
			"goods-list":goodsList,	
		},
		methods: {
			// 获取商品列表的数据
		}
	}
</script>

<style lang="scss">
	.goods{
		background: #eee;
	}
	.isOver {
		width: 100%;
		height: 50px;
		line-height: 50px;
		text-align: center;
		font-size: 28rpx;
		
	}
</style>
