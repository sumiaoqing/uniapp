<template>
	<view class="home_content">
		<view class="nav-swiper">
			<scroll-view scroll-x="true" class="swiper">
				<text v-for="item of navArr" class="nav-text">{{item}}</text>
			</scroll-view>
		</view>
		<view class="home_main">
			<view class="main-block" v-for="item in 3">
				<view class="user-mes">
					<view class="mes-avatar">

					</view>
					<view class="mes-nickname">
						昵称
					</view>
					<view class="mes-time">
						2019-01-09
					</view>
				</view>
				<view class="news-mes">
					帖子信息帖子信息帖子信息帖子信息帖子信息帖子信息帖子信息
				</view>
				<view class="news-img">
					<image src="../../static/pic/testImg.webp"  class="img-test"></image>
				</view>
				<view class="operating-list">
					<view class="list-block" v-for="item in listArr">
						{{item}}
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				navArr: ['关注', '推荐', '体育', '热点', '影视'],
				listArr:[1,2,3,'分享']
			}
		}
	}
</script>

<style>
	.home_content {
		display: flex;
		flex-direction: column;
	}

	.nav-swiper {
		height: 96rpx;
		background-color: red;
	}

	.nav-text {
		height: 96rpx;
		line-height: 96rpx;
		width: 180rpx;
		text-align: center;
		display: inline-block;
	}

	.swiper {
		height: 96rpx;
		width: 750rpx;
		white-space: nowrap;
	}

	.home_main {
		width: 100%;
		flex: 1;
		overflow-y: auto;
		display: flex;
		flex-direction: column;
	}

	.main-block {
		width: 100%;
		background-color: #4CD964;
	}

	.user-mes {
		height: 140rpx;
		width: 100%;
		background-color: #007AFF;
		position: relative;
	}

	.mes-avatar {
		position: absolute;
		width: 110rpx;
		height: 110rpx;
		transform: translateY(-50%);
		top: 50%;
		left: 20rpx;
		border-radius: 110rpx;
		background-color: #2C405A;
	}

	.mes-nickname {
		position: absolute;
		left: 150rpx;
		font-size: 34rpx;
		top: 20rpx;
	}

	.mes-time {
		position: absolute;
		left: 150rpx;
		font-size: 30rpx;
		bottom: 20rpx;
	}
	.news-mes{
		width: calc(100%-40rpx);
		padding-left: 20rpx;
	}
	.news-img{
		width: 100%;
		height: 280rpx;
		background-color: #007AFF;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.img-test{
		width: 710rpx;
		height: 240rpx;
		border-radius: 10rpx;
	}
	.operating-list{
		display: flex;
		flex-direction: row;
		width: 100%;
		height: 90rpx;
	}
	.list-block{
		flex: 1;
		height: 100%;
	}
</style>
