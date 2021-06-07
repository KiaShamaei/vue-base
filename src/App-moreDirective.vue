<template>
<!--because of v-once threat same as static ele -->
	<h2 v-once>{{name}}</h2>
	<button v-on:click="name = 'mahsa'">change name </button>

	<!--because of v-pre it doesnt compile  -->
	<h2 v-pre> {{name}}</h2>

</template>


<script>

export default ({
	data(){
		return {
			name: "kia"
		}
	}
})
</script>


<style scoped>

</style>