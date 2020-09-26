<template>
	<view class="content">
		<indexHeader></indexHeader>
		<view class="friends" v-for="(item,index) in friends" :key="item.id">
			<view class="pic">
				<image :src="`../../static/picture/${item.imgUrl}`"></image>
			</view>
			<view class="main">
				<view class="textTop">
					<view class="friendName">{{item.friendName}}</view>
					<view class="times">{{getTime(item.times)}}</view>
				</view>
				<view class="textBottom">
					{{item.msg}}
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import indexHeader from '../../components/header/indexHeader.vue'
	import datas from '../../commom/js/datas.js'
	import momentDate from '../../commom/js/myTime.js'
	export default {
		data() {
			return {
				title: 'Hello',
				friends: []
			}
		},
		components:{
			indexHeader,
		},
		onLoad() {
			this.getDatas();
		},
		methods: {
			getTime (dateTime){
				return momentDate.dateTime(dateTime);
			},
			jump() {
				uni.navigateTo({
					url:"../resources/resource"
				})
			},
			getDatas() {
				this.friends=datas.friends();
			}
		}
	}
</script>

<style lang="scss">
		.friends {
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
