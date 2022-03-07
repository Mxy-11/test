<template>	
	<topbar @tabItemClick="handleItemClick" :options="options" :tabItem="tabItem" :tabIndex="tabIndex" @click="toptab"></topbar>
</template>

<script>
	import topbar from '../../components/top-tabbar/top-tabbar.vue'
	export default{
		props:{
			tabIndex:{
				type:Number,
				default:0
			}
		},
		//监听参数(tabIndex)变化
		watch:{
			tabIndex(newval,oldval){
				console.log(newval,oldval)
			}
		},
		data(){
		    return {
		        options:{
		            top_backgroundcolor:'#00a0f0',
		            top_itemcolor:'#000000',
		            top_itemselectcolor:'#ffffff'
		        },
				midindex:0,
				// tabIndexx=tabIndex,
		        tabItem: [
		            {
		                name: '精选',
		                id: 2001
		            },
		            {
		                name: '男频',
		                id: 2002
		            },
					{
					    name: '女频',
					    id: 2003
					},
					{
					    name: '排行',
					    id: 2004
					}
		        ]
		    }
		},
		methods: {
		    handleItemClick(index) {
		        console.log('序号',index)
				this.midindex=index
				this.$emit('change',this.midindex)
		    },
			// toptab(midindex){
			// 	// this.midindex = e.tindex				
			// 	// console.log('点击日志',e)
			// 	midindex=index
			// 	this.$emit('toptabClick',midindex)
			// }
			// toptab(e){
			// 	console.log('dianji日志',e)
			// 	const{midindex}=e.index
			// 	console.log(midindex)
			// 	this.$emit('change',midindex)
			// }
		},
		components: {
			topbar
		}
		
	}	

</script>

<style lang="scss">
</style>
