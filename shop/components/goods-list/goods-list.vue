<template>
	<view>
		<view class="hot_goods">
			<view class="goods_list">
				<view class="goods_item" v-for="item in goods" :key="item.id">
					<image :src="item.url"></image>
					<view class="price">
						<text>￥{{item.price}}</text>
					</view>
					<view class="name">
						{{item.zhaiyao}}
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: ['goods'],
		data() {
			return {
			}
		}
	}
</script>

<style lang="scss">
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

		.goods_list {
			padding: 0 15rpx;
			display: flex;
			flex-wrap: wrap;
			justify-content: space-between;

			.goods_item {
				background: #fff;
				width: 355rpx;
				margin: 10rpx 0;
				padding: 15rpx;
				box-sizing: border-box;

				image {
					width: 80%;
					height: 150px;
					display: block;
					margin: auto;
				}

				.price {
					color: $shop-color;
					font-size: 36rpx;
					margin: 20rpx 0 10rpx 0;

					text:nth-child(2) {
						color: #ccc;
						font-size: 20rpx;
						margin-left: 17rpx;
						text-decoration: line-through;
					}
				}

				.name {
					font-size: 24rpx;
					line-height: 50rpx;
					padding-top: 10rpx;
				}
			}
		}
	}
</style>
