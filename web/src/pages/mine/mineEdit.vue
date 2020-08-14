<template>
	<view>
		<view class=" mineEdit">
			<image src="../../static/headpic.jpg" mode=""></image>
		</view>
		<form @submit="" @reset="">
			<uni-list>
				<uni-list-item title="昵称">
				</uni-list-item>
				<uni-list-item title="性别">
				</uni-list-item>
				<uni-list-item title="城市">
				</uni-list-item>
				<uni-list-item title="自我介绍"> </uni-list-item>

			</uni-list>
			<button form-type="submit" type="default">保存</button>
			<button form-type="reset">Reset</button>
		</form>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.mineEdit {
		display: flex;
		justify-content: center;
		align-items: center;

		image {
			width: 150rpx;
			height: 150rpx;
			border-radius: 50%;
			// margin: 10rpx auto;
		}
	}
</style>
