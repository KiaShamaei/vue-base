<template>
<h1> kia is bala ! {{name}}</h1>
<div v-text="lname"></div> 
<div v-html="camel"></div>
<div v-bind:id="headId"> this is a tag with heading id </div>
<button v-bind:disabled="disabled" v-on="handleChange">bind value </button>
<p v-bind:class="status"> this is p with dynamic class</p>

<!--this condition class  -->
<h2 v-bind:class = "ispromoted &&  'success'">this is condition </h2>
<!--conditional class array and obj -->
<h3 v-bind:class="[ispromoted && 'success', disabled ? 'align' :'' ]">this condition with array</h3>
<h2 v-bind:class = "{  'success' : ispromoted}">hi honey </h2>


<!-- inline style -->
<h3 v-bind:style="{
	color  : highlight, 
	'font-size' : fontHigh +'px',
	'background-color' :back 
}">Font and  color inline </h3>
<!-- inline with obj-->
<p v-bind:style="objStyle1">kia with obj style ---</p>
<div v-bind:style="[objStyle1,objStyle2]">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos, voluptas.</div>
</template>

<script>


export default {
  name: 'App',
 data (){
return {
	name :  "shamae" ,
	lname : "vishvas",
	camel : "<b>kia is good learner</b>",
	headId : "heading",
	disabled :  true,
	ispromoted : true , 
	status  : "success" , 
	highlight : 'crimson',
	back :  'blue',
	fontHigh : 30 ,
	objStyle1 :{
		font : '10px',
		color : 'crimson',
		backgroundColor :  'yellow'
	},
	objStyle2 :{
		fontSize : '40px',
		
	}
}

 },
//  methods: {
// 	 handleChange :function(){
// 		 this.status = "failed"
// 	 }

//  }


 }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.success {
	color : greenyellow ;
}
.failed {
	color : crimson;
}
.align{
	font-size: 400;
	background-color: coral ;
}
</style>
