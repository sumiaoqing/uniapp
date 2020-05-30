<template>
	<view class="login" @click="login">
		我是首页
	</view>
</template>

<script>
	export default
	{
		data() {
			return {
				title: 'Hellou你'		
			}
		},
		methods:{
			login()
			{
				console.log('999')
				uni.switchTab({
					url:'/pages/home/index'
				})
			}
		}
	}
</script>

<style>
</style>
