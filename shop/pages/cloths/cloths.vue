<template>
	<view class="cloths">
		<scroll-view scroll-y="true" class="left">
			<view 
				v-for="(item, index) in clothsCate"
				:key="item.id"
				:class="active === index? 'active':' '"
				@click="leftClickHandle(index, item.id)"
			>
				{{item.title}}
			</view>
		</scroll-view>
		<scroll-view scroll-y="true" class="right">
			<view class="item" v-for="(item, index) in clickData" :key="item.index">
				<image :src="item.url" @click="previewImage(item.url)"></image>
				<text>{{item.text}}</text>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				clothsCate: [
					{	
						id : 1,
						title: '晓晓出品'
					},
					{
						id : 2,
						title: '春潮来袭'
					},
					{
						id : 3,
						title: '小众'
					},
					{
						id : 4,
						title: '女鞋'
					},
					{
						id : 5,
						title: '正装鞋'
					},
					{
						id : 6,
						title: '潮鞋'
					},
					{
						id : 7,
						title: '晓晓自营'
					},
					{
						id : 8,
						title: '智能腕表'
					},
					{
						id : 9,
						title: '男鞋'
					},
					{
						id : 10,
						title: '上衣'
					},
					{
						id : 11,
						title: '裤装'
					},
					{
						id : 12,
						title: '内衣'
					},
					{
						id : 13,
						title: '奢侈品'
					},
					{
						id : 14,
						title: '运动'
					},
					{
						id : 15,
						title: '功能类'
					},
					{
						id : 16,
						title: '服配'
					},
					{
						id : 17,
						title: '衬衫'
					},
					{
						id : 18,
						title: '卫衣'
					},
					{
						id : 19,
						title: '皮衣'
					},
					{
						id : 20,
						title: '羊毛衫'
					}
				],
				active: 0,
				rightDate: [
					{
						id: 1,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/98983/25/16598/202926/5e7da468E23a636f6/ae88aa976df65991.jpg!cr_1125x445_0_171!q70.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/98983/25/16598/202926/5e7da468E23a636f6/ae88aa976df65991.jpg!cr_1125x445_0_171!q70.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 2,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 3,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 4,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 5,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 6,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 7,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 8,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 9,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 10,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 11,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 12,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 13,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 14,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 15,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 16,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 17,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 18,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 19,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					},
					{
						id: 20,
						data: [
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							},
							{
								url : 'http://m.360buyimg.com/mobilecms/s700x280_jfs/t1/92957/18/17126/99290/5e842ddbE7aa1484e/cabd163b4eee3a28.jpg',
								text: '111'
							}
						]
						
					}
				],
				clickData: ''
			}
		},
		onLoad() {
			this.leftClickHandle(0, this.clothsCate[0].id)
		},
		methods: {
			leftClickHandle(index, id) {
				console.log(index, id)
				this.active = index
				const rightDate = this.rightDate
				console.log(rightDate[index].data)
				this.clickData = rightDate[index].data
			},
			previewImage (current) {
				const urls =this.clickData.map(item=>{
					return item.url
				})
				console.log(urls)
				uni.previewImage({
					urls,
					current
				})
			}
		}
	}
</script>

<style lang="scss">
	page{
		height: 100%;
	}
	
	.cloths{
		height: 100%;
		display: flex;
		.left{
			width: 200rpx;
			height: 100%;
			border-right: 1px solid #eee;
			view{
				height: 50px;
				line-height: 50px;
				color: #333;
				text-align: center;
				font-size: 30rpx;
				border-top: 1px solid #eee;
			}
			.active {
				background-color: $shop-color;
				color: #fff;
			}
		}
	}
	.right{
		height: 100%;
		width: 520rpx;
		margin: 0 auto;
		.item{
			image{
				width: 530rpx;
				height: 520rpx;
				border-radius: 10px;
			}
			text{
				font-size: 30rpx;
				line-height: 60rpx;
			}
		}
	}
</style>
