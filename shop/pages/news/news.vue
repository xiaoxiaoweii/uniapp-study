<template>
	<view class="news">
		<news-item :newsData="newsData" @itemClick="goDetail"></news-item>
	</view>
</template>

<script>
	import newsItem from '../../components/news-item/news-item'
	export default {
		data() {
			return {
				newsData: [
					{
						time: '2020-01-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img31.house365.com/M00/0C/63/rBEBYF5gjYmANGx2AAEr7KKlmv4143_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '珍珠花苑2室2厅1卫165万元77.46平方',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					},
					{
						time: '2019-10-11',
						see: '122',
						title: '双南 一北 客厅大 97年房龄 业主诚心出售',
						url: 'http://img34.house365.com/M03/29/1C/rBEBp159dwqALjYJAAH-a8xXv44544_240x170_c.jpg'
					}
				]
			}
		},
		components:{
			"news-item": newsItem
		},
		methods: {
			goDetail() {
				uni.navigateTo({
					url: '/pages/news-detail/news-detail'
				})
			}
		}
	}
</script>

<style lang="scss">
</style>
