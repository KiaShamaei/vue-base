<template>
	<div>
		<h2>This is from component C {{username}}</h2>

	</div>
</template>

<script>
	export default {
		name : "ComponentC" ,
		inject : ['username']
	}
</script>

<style lang="scss" scoped>

</style>