<template>
	<view>
	<view class="example-body">
				<uni-nav-bar :fixed="false" color="#333333" background-color="#00a0f0">
	<!-- 			<block slot="left">
					</block> -->
					<view class="bar-return" @click="returnhandle">
						<uni-icons type="left-nav" size="30"></uni-icons>
					</view>
					<view class="input-view">
						<uni-icons class="input-uni-icon" type="search" size="22" color="#666666" />
						<input confirm-type="search" class="nav-bar-input" type="text" placeholder=" 输入搜索关键词" @confirm="confirm" />
					</view>
					<view class="searchbutton">搜索</view>
				</uni-nav-bar>
			</view>	
	</view>
</template>

<script>
	import uniNavBar from '@/components/uni-nav-bar/uni-nav-bar.vue'
	export default {
		name:"navbar",
		data() {
			return {
				
			};
		},
		components: {
			uniNavBar
		},
		methods:{
			returnhandle(){
				uni.navigateBack({
					delta:1
				})
			}

		}
	}
</script>

<style lang="scss">
$nav-height: 30px;
	.input-view {
		/* #ifndef APP-PLUS-NVUE */
		display: flex;
		/* #endif */
		flex-direction: row;
		width: 480rpx;
		flex: 1;
		// background-color: $uni-bg-color-grey;
		background-color: $uni-bg-color-grey;
		height: $nav-height;
		border-radius: 10px;
		padding: 0 15px;
		flex-wrap: nowrap;
		margin: 7px 0;
		line-height: $nav-height;
	}
	
	.input-uni-icon {
		line-height: $nav-height;
	}
	
	.nav-bar-input {
		height: $nav-height;
		line-height: $nav-height;
		/* #ifdef APP-PLUS-NVUE */
		width: 300rpx;
		/* #endif */
		padding: 0 5px;
		font-size: $uni-font-size-base;
		background-color: $uni-bg-color-grey;
	}
	.searchbutton{
		width: 90rpx;
		padding: 0 10px;
	}
	.bar-return{
		width: 70rpx;
		padding: 0 1px;
	}
	
	.example-body {
		/* #ifndef APP-NVUE */
		display: flex;
		justify-content: space-around;
		margin: auto;
		/* #endif */
		padding: 0;
	}
</style>
