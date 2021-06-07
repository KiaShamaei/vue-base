<template>
	<div>
		<h2>This is app part username  :  {{name}}</h2>
		<ComponentA />

	</div>
</template>

<script>
import ComponentA from './components/ComponentTree/ComponentA'
	export default {
		name : "App",
	
		components :{
			ComponentA
		},
		data(){
			return {name : 'vishWas'}
		},
		provide(){
			return {
			username : this.name
			}
		}
		
	}
</script>

<style lang="scss" scoped>

</style>