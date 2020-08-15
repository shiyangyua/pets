<template>
	<view>
		<view class="header">
			<image src="../../static/headpic.jpg" mode=""></image>
			<view class="name">
				<span>Oxygen    </span>
				<uni-icons type="weibo" @click="goMineEdit"></uni-icons>
			</view>

		</view>
		<uni-list>
			<uni-list-item @click="goMyPub">我发布的领养</uni-list-item>
			<uni-list-item @click="goMyRequest">我申请的领养</uni-list-item>
			<uni-list-item>我的打卡记录</uni-list-item>
		</uni-list>
	</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			goMyPub() {
				uni.navigateTo({
					url: "myPublish"
				})
			},
			goMineEdit(){
				uni.navigateTo({
					url:'mineEdit'
				})
			},
			goMyRequest(){
				uni.navigateTo({
					url:'myRequest'
				})
			}
		}
	}
</script>

<style lang="scss">
	.header {
		display: flex;

		// flex-wrap: wrap;
		.name {
			// line-height: 150rpx;
			margin: auto 0;
		}

		image {
			width: 150rpx;
			height: 150rpx;
			border-radius: 50%;
			margin: 50rpx 30rpx;
		}
	}
</style>
