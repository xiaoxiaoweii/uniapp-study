<template>
	<view class="cloths">
		<scroll-view scroll-y="true" class="left">
			<view 
				v-for="(item, index) in clothsCate"
				:key="item.id"
				:class="active === index? 'active':' '"
				@click="leftClickHandle(index)"
			>
				{{item.title}}
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
				active: 0
			}
		},
		methods: {
			leftClickHandle(index) {
				console.log(index)
				this.active = index
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
</style>
