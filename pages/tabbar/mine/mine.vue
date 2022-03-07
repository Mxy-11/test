<template>
	<view>
		<view class="advertcard">
			<view class="advertcard-T">
				<view class="advertcard-Ta">免广告特权</view>
				<view class="advertcard-Tb">暂未享受广告特权</view>
			</view>
			<view class="advertcard-share">
				<view class="advertcard-share-num">已推广0人</view>
				<view class="advertcard-share-a">
					<view class="advertcard-share-a-butt">
						<view class="advertcard-share-a-buttT">分享推广</view>
					</view>
					<view class="advertcard-share-a-t">
						<view class="advertcard-share-a-ta">分享可得终身免广告特权</view>
						<view class="advertcard-share-a-ticon">
							<uni-icons type="arrowrightcricle" size="15"></uni-icons>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.advertcard{
		display: flex;
		padding: 5px;
		margin: 10px;
		border-radius: 4px;
		box-shadow: 0 0 3px 1px #cecece;
		box-sizing: border-box;
		background-color:#f8f8f8;
		justify-content:center;
		flex-direction:column;
		.advertcard-T{
			display: flex;
			padding: 3px;
			margin-bottom: 7px;
			//margin: 5px;
			height: 20px;
			background-color: #ffffff;
			flex-direction:row;
			justify-content:space-between;
			.advertcard-Ta{
				margin: 4px;
			}
			.advertcard-Tb{
				margin: 4px;
			}
		}
		.advertcard-share{
			display: flex;
			padding: 10px;
			margin: 5px;
			margin-right:1px;
			margin-left: 1px;
			background-color: #ff6f6a;
			justify-content:space-between;
			align-items: center;
			border-radius:10px;
			.advertcard-share-num{
				display: flex;
				padding: 3px,6px;
				margin: 3px;
				justify-content:start;
				color: #FFFFFF;
			}
			.advertcard-share-a{
				display: flex;
				flex-direction: column;
				.advertcard-share-a-butt{
					border-radius:12px;
					margin-bottom: 5px;
					padding: 1px;
					display: flex;
					width: 100px;
					height: 30px;
					flex-direction: column;
					background-color: #ffffff;
					justify-content:center;
					align-content:center;
					margin-left:auto;
					.advertcard-share-a-buttT{
						display: flex;
						justify-content:center;
						align-items: center;
						color: #ff6f6a;
					}
				}
				.advertcard-share-a-t{
					display: flex;
					width: 180px;
					//margin: 3px;
					//padding: 8px 0px;
					margin-top: 3px;
					flex-direction: row;
					justify-content:center;
					margin-left:auto;
					.advertcard-share-a-ta{
						color: #ffffff;
					}
					.advertcard-share-a-ticon{
						
					}
				}

			}
	
		}

	}

</style>
