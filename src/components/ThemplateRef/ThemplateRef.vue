<template>
	<div>
		<input type="text" ref="inputref">
		<Posts ref="Posts"/>
	</div>
</template>

<script>
import Posts from "../Http/Posts.vue"
	export default {
		name:"ThemplateRef",
		components : {
			Posts

		},
		mounted(){
			this.$refs.inputref.focus();
			console.log(this.$refs.Posts)

		}
		
	}
</script>

<style lang="scss" scoped>

</style>