<template>
	<view>
		<view class="listcard">
			<view class="listcard-image">
				<image src="../../static/logo.png" mode=""></image>
			</view>
			<view class="listcard-content">
				<view class="listcard-content_title">书名</view>
				<view class="listcard-content_des">
					<view class="listcard-content_des-updateCap">最新章节</view>
					<view class="listcard-content_des-updateDate">
						<view class="listcard-content_des-updateDate-icon">
							<uni-icons type="arrowrightcricle" size="15"></uni-icons>
						</view>
						<view class="listcard-content_des-updateDate-num">2021-9-27</view>
					</view>
				</view>
			</view>
			<view class="listcard-icon">
				<uni-icons type="more-filled" size="30"></uni-icons>
			</view>
		</view>
	</view>
</template>

<script>
	import uniIcons from "@/components/yangxiaochuang-icons/yangxiaochuang-icons.vue"
	export default {
		components: {uniIcons},
		name:"list-card",
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.listcard{
		display: flex;
		padding: 10px;
		margin: 10px;
		border-radius: 1px;
		box-shadow: 0 0 3px 1px #999999;
		box-sizing: border-box;
		.listcard-image{
			flex-direction: 0;
			width: 80px;
			height: 70px;
			overflow: hidden;
			border-radius: 5px;
			image{
				width: 100%;
				height: 100%;
			}
		}
		.listcard-content{
			display: flex;
			flex-direction: column;
			padding-left: 10px;
			width: 100%;
			.listcard-content_title{
				color: #333333;
				font-size: 17px;
				font-weight: 500;
				line-height: 1.2;
			}
			.listcard-content_des{
				display: flex;
				flex-direction: column;
				justify-content: space-between;
				font-size: 12px;
				.listcard-content_des-updateCap{
					padding: 8px 0px;
					margin-right: 6px;
				}
				.listcard-content_des-updateDate{
					display: flex;
					flex-direction: row;
					justify-content: flex-start;
					font-size: 12px;
					.listcard-content_des-updateDate-icon{
						// display: flex;
					}
					.listcard-content_des-updateDate-num{
						display: flex;
					}
				}
			}
		}
		.listcard-icon{
			// style="height: 40px; 
			// background-color: #FFFFFF;
			display: flex; 
			flex-direction: row; 
			align-items: center;
		}
	}

</style>
