<template>
	<div>
		<h2>this is popup ...</h2>
		<button v-on:click="$emit('close',name)">close popup</button>
		<input type="text" name="name" id="name" v-model="name">

	</div>
</template>

<script>
console.log("pop----------")
	export default {
		name : "Pop",
		emits : {
			close : (name)=>{
				if(!name)
				return false;
				return true;
			}
		}
	}
</script>

<style lang="scss" scoped>

</style>