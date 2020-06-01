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
		mounted()
		{
			let socket=uni.connectSocket({
				url:'http://192.168.1.2:3000/',
				success()
				{
					console.log('socket连接成功')
				}
			})
			socket.onOpen((res)=>
			{
				console.log('连接正常');
				socket.send({
					data:'uuuuu'
				})
			})
			socket.onMessage((res)=>{
				console.log(res,'收到的信息')
			})
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
