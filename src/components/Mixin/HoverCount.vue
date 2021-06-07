<template>
	<div>
		<p v-on:mouseover="handleInc">inc --- {{count}}</p>
	</div>
</template>

<script>
import mixins from './mixin'
	export default {
		name : 'HoverCount',
		mixins : [mixins]

	}
</script>

<style lang="scss" scoped>

</style>