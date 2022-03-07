<template>
		<swiper class="home-swiper" @change="change" :current="defaultIndex">
			<swiper-item class="swiper-item">
				<list-item></list-item>
			</swiper-item>
			<swiper-item class="swiper-item">
				<list-item></list-item>
			</swiper-item>			
			<swiper-item class="swiper-item">
				<list-item></list-item>
			</swiper-item>
			<swiper-item class="swiper-item">
				<list-item></list-item>
			</swiper-item>
		</swiper>
</template>

<script>
	
	import listItem from './list-item.vue'
	export default {		
		components:{
			listItem
		},
		name:"list",
		props:{
			tab:{
				type:Array,
				default(){
					return[]
				}
			},
			defaultIndex:{
				type:Number,
				default:0
			}
		},
		data() {
			return {
				
			};
		},
		methods:{
			change(e){
				console.log('滑动日志',e)
				const{current}=e.detail
				this.$emit('change',current)
			}
			
		}
	}
</script>

<style lang="scss">
	.home-swiper{
		height: 100%;
		.swiper-item{
			height: 100%;
			overflow: hidden;
			.list-scroll{
				height: 100%;
			}
		}
	}

</style>
