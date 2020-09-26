<template>
	<view class="content">
		<indexHeader></indexHeader>
		<view class="msg">
			<view class="pic">
				<image src="../../static/picture/pic1.jpg"></image>
			</view>
			<view class="main">
				<view class="textTop">
					<view class="friendName">美乐蒂</view>
					<view class="times">中午13:14</view>
				</view>
				<view class="textBottom">
					wowwowwowwowwowwowwowwowwwow
				</view>
			</view>
		</view>
		<view class="msg">
			<view class="pic">
				<image src="../../static/picture/haha.png"></image>
			</view>
			<view class="main">
				<view class="textTop">
					<view class="friendName">靓丽美女</view>
					<view class="times">上午05:20</view>
				</view>
				<view class="textBottom">
					Good Morning!!
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import indexHeader from '../../components/header/indexHeader.vue'
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		components:{
			indexHeader,
		},
		onLoad() {

		},
		methods: {
			jump() {
				uni.navigateTo({
					url:"../resources/resource"
				})
			}
		}
	}
</script>

<style lang="scss">
		.msg {
			display: flex;
			width: 750rpx;
			.pic {	
				width: 160rpx;
				height: 160rpx;
				image {
					width: 96rpx;
					height: 96rpx;
					left:50%;
					top:50%;
					transform: translate(-50%,-50%);
					border-radius: 12rpx;
					
				}
			}
			.main {
				width: 590rpx;
				display: flex;
				flex-direction: column;		
				.textTop {
					flex: 1;
					display: flex;
					justify-content: space-between;
					align-items: flex-end;
					.friendName {
						font-size: 38rpx;
						color: #272832;
					}
					.times {
						padding-right: 30rpx;
						padding-bottom:10rpx;
						font-size: $uni-font-size-sm;
						color: #272832;
						opacity: 0.5;
					}
				}
				.textBottom {
					flex: 1;
					white-space: nowrap;
					overflow: hidden;
					text-overflow: ellipsis;
					padding-right: 30rpx;
					font-size: 32rpx;
					color: #272832;
					opacity: 0.6;
				}
			}
		}
</style>
