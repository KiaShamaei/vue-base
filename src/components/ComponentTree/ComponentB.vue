<template>
	<div>
		<h2>This from CB</h2>
		<ComponentC />

	</div>
</template>

<script>
import ComponentC from './ComponentC'
	export default {
		name : "ComponentB",
		components : {ComponentC }
	}
</script>

<style lang="scss" scoped>

</style>