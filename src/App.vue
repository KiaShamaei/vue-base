<template>
	<div>
	 <HoverCount />
	 <ClickCount />
 
	</div>
</template>

<script>
import HoverCount from './components/Mixin/HoverCount.vue';
import ClickCount from './components/Mixin/ClickCount.vue'
	export default {
		name : 'App',
		components : {
			HoverCount,
			ClickCount
		}
	}
</script>

<style lang="scss" scoped>

</style>