<template>
	<h2> full name with mustash {{name}} - {{lname}}</h2>
	<h2>full name with computed {{fullname}}</h2>
	<button v-on:click ="items.push({id : 6 , price : 100})">add item </button>

	<p>this is one the usage of computed :  {{totalShow}}</p>
	<p>this is from normal method to show render part {{getTotal()}}</p>
	<input type="text" v-model="current">
<!--conditional list rendering -->
<div v-for="item in items" :key="item.id">
	<p v-if="item.price > 100">{{item.id}}</p>
</div>
<!--conditional rendering with computed-->
<h3 v-for ="item in expensiveSelect " :key="item.id">
	{{item.id}} --- {{item.price }}
</h3>


</template>


<script>


export default ({
	data() {
		return {
			name : "kia",
			lname :  "shamaei",
			items :[
				{id:1, price:120 },
				{id:2, price:100 },
				{id:3, price:110 },
				{id:4, price:80 },
				{id:5, price:90 },
			],
			current :  ""
		}
	},
	methods : {
		getTotal  (){
			console.log("normal methods--- ")
			return this.items.reduce((total, current)=> total = total + current.price, 0)
		}
	},
	computed:{
		fullname(){
			return `${this.name} - ${this.lname}`
		},
		totalShow(){
			console.log("computed methods ---")
			return this.items.reduce((total,current)=>total=total + current.price,0)
		},
		expensiveSelect(){
			return this.items.filter(item=>item.price >  100)
		}
	}
})
</script>
<style scoped>

</style>