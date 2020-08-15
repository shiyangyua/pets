<template>
	<view>
		<form @submit="" @reset=""class="editForm">
			<view class=" mineEdit">
				<image src="../../static/headpic.jpg" mode=""></image>
			</view>
			<view class="formItem">
				<view class="itemLabel">
					昵称：
				</view> <input type="text" value="oxygen" />
			</view>
			<view class="formItem">
				<view class="itemLabel">性别：</view>
				<view class="itemMain">
					<picker @change="bindPickerChange" :value="sexIndex" :range="sex">
						<view class="uni-input">{{sex[index]}}</view>
					</picker>
				</view>
			</view>
			<view class="formItem">
				<view class="itemLabel"> 城市： </view>
					<view class="itemMain">
						<picker @change="bindPickerChange" :value="index" :range="array">
							<view class="uni-input">{{array[index]}}</view>
						</picker>
					</view>
			</view>
			<view  class="formItem">
				自我介绍：
			</view> <textarea value="" placeholder="" />
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
				sex:['男', '女','未知'],
				sexIndex: 0,
			}
		},
		methods: {
			bindPickerChange: function(e) {
				console.log('picker发送选择改变，携带值为', e.target.value)
				this.index = e.target.value
			}
		}
	}
</script>

<style lang="scss" scoped>
.editForm{
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
	.formItem{
		display: flex;
		margin: 30rpx 0 25rpx 30rpx;
		border-bottom: 1rpx solid #CCCCCC;
		.itemLabel{
			margin: 0rpx 20rpx 0rpx 0rpx;
			color: #CCCCCC;
		}
		.itemMain{
			
		}
		// textarea{
		// 	border: 1px solid #CCCCCC;
		// 	margin: 5rpx 10rpx 20rpx 5rpx;
		// 	height: 100rpx;
		// 	width: 90%;
		// }
	}
}
</style>
