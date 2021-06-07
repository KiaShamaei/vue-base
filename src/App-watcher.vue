<template>
<h2>the prop data value ----->  {{valume}}</h2>
	<button v-on:click="valume += 1">Inc</button>
	<button v-on:click="valume -= 1">Dec</button>
	<input type="text" v-model="movie">
	<input type="text" v-model.lazy="movieInfo.name">
	<input type="text" v-model.lazy="movieInfo.actor">
</template>
<script>


export default ({
	data(){
		return {
			valume : 0,
			movie : "batman",
			movieInfo : {
				name :  "",
				actor :  ""
			}
		}
	},
	watch : {
		valume(newvalue , prevalue){
			if ( newvalue === 5 && newvalue > prevalue){
			alert("value of voloom is more than 15")
			}

		},
		movie: {
			handler(newvalue){
				console.log(newvalue)
			}, 
			immediate :  true
		},
		movieInfo :  {
			handler (newMovie){
				console.log("this is work only with deep prop" , newMovie.name , newMovie.actor)
			}
			,deep : true
		}
	}
})
</script>
<style scoped>

</style>