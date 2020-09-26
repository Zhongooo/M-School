<template>
	<view class="header">
		<view class="left">
			<image src="../../static/picture/pic2.jpg"></image>
		</view>
		<view class="middle">
			<image src="../../static/icon/火.png"></image>
		</view>
		<view class="right">
			<image src="../../static/icon/search.png" class="search"></image>
			<image src="../../static/icon/addgroup.png" class="add"></image>
		</view>
	</view>
</template>

<script>
</script>

<style lang="scss">
	.header {
		display: flex;
		width: 750rpx;
		height: 88rpx;
		border-bottom: 1rpx solid whitesmoke;
		.left {
			flex:1;
			image {
				width: 68rpx;
				height: 68rpx;
				margin-left:32rpx;
				margin-top:8rpx;
				border-radius: 10%;
			}
		}
		.middle {
			flex:2;
			display: flex;
			justify-content: center;
			align-items: center;
			image {
				width: 88rpx;
				height: 42rpx;
			}
		}
		.right {
			flex:1;
			display: flex;
			justify-content: space-around;
			align-items: center;
			.search {
				width: 52rpx;
				height: 52rpx;
			}
			.add {
				width: 48rpx;
				height: 48rpx;
			}
		}
	}
</style>
