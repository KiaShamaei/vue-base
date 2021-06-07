<template>
	<div>
		<button v-on:click="handleInc">inc --- {{count}}</button>
	</div>
</template>

<script>
import mixins from './mixin'
	export default {
		name : 'ClickCount',
		mixins : [mixins]
	
	}
</script>

<style lang="scss" scoped>

</style>