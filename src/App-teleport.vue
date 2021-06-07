<template>
	<div>
		<p>this is in app rout</p>
		<teleport to="#portal">
			<Portal/>

		</teleport>

	</div>
</template>

<script>
import Portal from './components/Portal'
	export default {
		name : 'App',
		components : {
			Portal
		}
	}
</script>

<style lang="scss" scoped>

</style>