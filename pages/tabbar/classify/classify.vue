<template>
	<view class="page">
		雨峰服了
		<view class="menu">
			<view class="leftScroll">
				<view
				:class="isActive==index?'itemLeftTwo':'itemLeft'"
				:style="" v-for="(item,index) in leftItems"
				:key="index"
				@click="chooseClick(index)">
				{{item.val}}
				</view>
			</view>
			<view class="rightScroll">
				<view class="bigConScro" v-for="(item,index) in array" :key="index">
					<view class="botCitysList">
						<view 
						class="listItems" 
						v-for="(items,index) in array[0].list " 
						:key="index">
						 {{items.name}}
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
			  isActive: 0,
			  leftItems:[
				{val:'全部分类'},
				{val:'男生'},
				{val:'女生'},
				{val:'press'},
			  ],
			  site:[
				{val:'全部分类', list:[]},
				{val:'男生', list:[]},
				{val:'女生', list:[]},
				{val:'press', list:[]},
			  ],
			  array:[]
			}
		},
		created() {
		    // 初始化数据默认选中第一个
			this.array.push(this.site[0])
		},
		mounted() {
			uni.request({
				url:"https://api.zhuishushenqi.com/cats/lv2/statistics",
				success:(res) =>{
					console.log(res.data)
					console.log(this.site[0].list)
					this.site[0].list=res.data.picture
					console.log(this.site[0].list)
					this.site[1].list=res.data.male
					this.site[2].list=res.data.female
					this.site[3].list=res.data.press
				}
			})
		},
		methods: {
			chooseClick(index) {
			  this.array = []
			  this.isActive = index;
			  this.array.push(this.site[index])
			},
		}
	}
</script>

<style lang="scss" scoped>
    .page {
        .menu {
            margin-top: 20rpx;
            padding: 0 15px;
            display: flex;
            .leftScroll {
                font-size: 28rpx;
                font-weight: 400;
                .itemLeft{
                    width: 186rpx;
                    height: 80rpx;
                    line-height: 80rpx;
                    padding-left: 28rpx;
                    color: #333333;
                    background-color: #F3F3F3;
                }
                .itemLeftTwo {
                    width: 178rpx;
                    height: 80rpx;
                    line-height: 80rpx;
                    padding-left: 28rpx;
                    background-color: #E2EDFF;
                    color: #2F77F1;
                    border-left: 4px solid #2F77F1;
                }
            }
            .rightScroll {
                background-color: #FFFFFF;
                width: 502rpx;
                height: 1076rpx;
                .bigConScro{
                    padding: 0 30rpx;
                    .topTitle{
                        margin-top: 20rpx;
                        font-size: 28rpx;
                        font-weight: 400;
                        color: #333333;
                    }
                    .botCitysList{
                        display: flex;
                        flex-wrap: wrap;
                        justify-content: space-between;
                        font-size: 24rpx;
                        font-weight: 400;
                        color: #333333;
                        margin-top: 44rpx;
                        .listItems{
                            margin-bottom: 20rpx;
                        }
                    }
                }
            }
        }
    }
</style>