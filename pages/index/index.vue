<template>
	<view class="content">
		<view class="text-area" @click="sayHi">



			{{title}}


		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hellou你66'		
			}
		},
		onLoad() {

		},
		methods: {
			sayHi() {
				console.log('000')
				uni.navigateTo({
					url: '/pages/login/index.vue'
				})
				console.log('22')

			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
