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
					<view>			<!-- 地区选择器 -->
						<view class="uni-list-cell-db">
							<picker @change="bindPickerChange" :value="index" :range="array">
								<view class="uni-input">{{array[index]}}</view>
							</picker>
						</view>
					</view>
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
				title: 'picker',
				array: ['中国', '美国', '巴西', '日本'],
				index: 0,
			}
		},
		methods: {
			selectPosition() {},
			bindPickerChange: function(e) {
				console.log('picker发送选择改变，携带值为', e.target.value)
				this.index = e.target.value
			}
		}
	}
</script>

<style lang="scss" scoped>
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
uni-list{
	uni-list-item{
		width: 100%;
		display: flex;
		// flex-direction: ;
	}
}
</style>
