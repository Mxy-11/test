<template>
	<view class="home">
		<Navbar></Navbar>
		<Toptab @change="toptabclick" :tabIndex="tabIndex"></Toptab>
		<view class="home-list">			
			<list @change="change" :defaultIndex="defaultIndex"></list>
		</view>
		

		
	</view>

</template>

<script>
	import Toptab from "../../../components/toptab/toptab.vue"
	import Navbar from "../../../components/navbar/navbar.vue"
	// import Content from "../../../components/list-scroll/list-scroll.vue"
	export default {
		data() {
			return{
				tabIndex:0,
				defaultIndex:0,				
			}
		},
		methods:{
			change(current){
				console.log('当前序号',current)
				this.tabIndex=current
			},
			toptabclick(midindex){
				console.log('标签',midindex)
				this.defaultIndex=midindex
			}
			
		},
		components: { 
			Toptab,
			Navbar
		}
	
	}
</script>

<style lang="scss">

	page{
		height:100%;
		display:flex;
	}
	.home{
		display:flex;
		flex-direction: column;
		flex: 1;
		// border: 1px red solid;
		overflow: hidden;
		.home-list{
			flex: 1;
			box-sizing: border-box;
		}

	}
</style>
