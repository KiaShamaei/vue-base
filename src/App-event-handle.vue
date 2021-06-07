<template>

<h2>Add methods and handling event to Vue :</h2>
<p> add ----> {{add(10,5)}}</p>
<p>function use data value --------{{mutiple(5)}}</p>

<button v-on:click="addCounter()">add to count </button>
<button v-on:click="addFiveCounter(5)">add5 </button>
<button @click="addShortHand()">add with shorthand</button>



<button v-on:click="count = count - 1">sub</button>
<button v-on:mouseover="name = 'vishvas'">change name</button>
<p>this is the count {{count}}</p>
<h3>{{name}}</h3>
<input v-model="message" placeholder="edit me">
<p>Message is: {{ message }}</p>
	
</template>

<script>
export default {
	name: "App",
	data(){
		return {
			baseVlue : 2,
			count : 5,
			name : 'kia',
			message : ""
			// nameChange : ""

		}
	},
	methods : {
		add(a, b){
			return a+b
		},
		mutiple(a){
			return a* this.baseVlue
		}, 
		addCounter(){
			this.count ++ ;
		},
		addFiveCounter(num){
			this.count += num  
		},
		addShortHand(){
			this.count ++
		}, 
		chageHandler (event){
			console.log(event);
			
		}


	},
	
}

</script>

<style>


</style>
