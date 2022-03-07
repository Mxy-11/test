<template>
	<view>
	<view class="example-body">
				<uni-nav-bar :fixed="false" color="#333333" background-color="#00a0f0" @clickLeft="showCity" @clickRight="scan">
	<!-- 			<block slot="left">
					</block> -->
					<view class="input-view"@click="searchHandle">
						<uni-icons class="input-uni-icon" type="search" size="22" color="#666666" />
						<input confirm-type="search" class="nav-bar-input" type="text" placeholder=" 输入搜索关键词" @confirm="confirm" />
					</view>
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
			searchHandle(){
			uni.navigateTo({
				url:"/pages/booksearch/search/search"
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
		width: 600rpx;
		flex: 1;
		// background-color: $uni-bg-color-grey;
		background-color: $uni-bg-color-grey;
		height: $nav-height;
		border-radius: 10px;
		padding:0 15px;
		flex-wrap: nowrap;
		margin: 7px 0;
		line-height: $nav-height;
	}
	
	.input-uni-icon {
		line-height: $nav-height;
		margin: 2px 0 0 0;
	}
	
	.nav-bar-input {
		height: $nav-height;
		line-height: $nav-height;
		/* #ifdef APP-PLUS-NVUE */
		width: 370rpx;
		/* #endif */
		padding: 0 5px;
		font-size: $uni-font-size-base;
		background-color: $uni-bg-color-grey;
	}
	
	.example-body {
		/* #ifndef APP-NVUE */
		display: block;
		/* #endif */
		padding: 0;
	}
</style>
