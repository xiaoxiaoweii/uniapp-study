<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@font-face {font-family: "iconfont";
	  src: url('~@/static/font/iconfont.eot?t=1585831501626'); /* IE9 */
	  src: url('~@/static/font/iconfont.eot?t=1585831501626#iefix') format('embedded-opentype'), /* IE6-IE8 */
	  url('data:application/x-font-woff2;charset=utf-8;base64,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') format('woff2'),
	  url('~@/static/font/iconfont.woff?t=1585831501626') format('woff'),
	  url('~@/static/font/iconfont.ttf?t=1585831501626') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+ */
	  url('~@/static/font/iconfont.svg?t=1585831501626#iconfont') format('svg'); /* iOS 4.1- */
	}
	
	.iconfont {
	  font-family: "iconfont" !important;
	  font-size: 16px;
	  font-style: normal;
	  -webkit-font-smoothing: antialiased;
	  -moz-osx-font-smoothing: grayscale;
	}
	
	.icon-quan:before {
	  content: "\e748";
	}
	
	.icon-zhuanqian:before {
	  content: "\e63d";
	}
	
	.icon-weibiaoti2fuzhi03:before {
	  content: "\e611";
	}
	
	.icon-icon-test:before {
	  content: "\e621";
	}
	
	.icon-tubiaolunkuo-:before {
	  content: "\e608";
	}
	
	.icon-fuwu:before {
	  content: "\e617";
	}
	
	.icon-coat:before {
	  content: "\e64c";
	}
	
	.icon-shengxian_xie:before {
	  content: "\e624";
	}
	
	
</style>
