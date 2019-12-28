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
		},
		onError:function(){
			console.log('App is Error!!')
		},
		onUniNViewMessage:function(){
			console.log('监听nvue页面发送的数据')
		}
	}
</script>

<style>

	/*每个页面公共css */

</style>
