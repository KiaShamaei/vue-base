<template>
	<div>
		<h2>This is from CA</h2>
		<ComponentB />


	</div>
</template>

<script>
import ComponentB from './ComponentB'
	export default {
		name : "ComponentA",
		components : {ComponentB}
	}
</script>

<style lang="scss" scoped>

</style>