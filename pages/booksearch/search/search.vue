<template>
	<view class="bar">
		<NavbarX></NavbarX>
	</view>
</template>

<script>
	import NavbarX from "../../../components/navbar/navbar-x.vue"
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		},
		components: {
			NavbarX
		}
	}
</script>

<style lang="scss">
	$nav-height: 30px;	
	.bar{
		display: flex;
		flex-direction: row;
	}
</style>
