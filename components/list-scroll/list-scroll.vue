<template>


			
			<view class="scroll">
				<scroll-view scroll-y="true" class="list-scroll">
					<!-- 纵向滚动 -->
					<view>
						<!-- <view v-for="item in 100">{{item}}</view> -->
						<slot></slot>
					</view>
				</scroll-view>
			</view>
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

	.scroll{
		flex: 1;
		overflow: hidden;
		box-sizing: border-box;
		.list-scroll{
			height: 100%;
			display: flex;
			flex-direction: column;
		}
	}

</style>
