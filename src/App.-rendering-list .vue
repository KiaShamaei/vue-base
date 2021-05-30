<template>

<h3 v-if="isShow">this test for condition </h3>
<h3 v-if="num === 6">this test for condition </h3>

<h3 v-else-if="num < 5">this test for condition </h3>
<h3 v-if="num === 5">this test for {{num}} </h3>
<!-- if we want to cancel more than one elements-->
<!-- <template v-if="isShow">
	<p> Lorem ipsum dolor sit amet.</p>
	<p>Lorem ipsum dolor sit amet.</p>
	<p>Lorem ipsum dolor sit amet.</p>	
</template> -->
<ul >
	<li v-for="name in names" :key="name">{{name}}</li>
	<li v-for="(name,index) in names" :key="index">{{name}}</li>
</ul>
<ul>
	<li v-for="(name,index) in fullnames" :key="index">{{name.fname}} - --- {{name.lname}}</li>
</ul>


<h2>kia is balaei pesar</h2>
  
</template>

<script>
export default {
	name : "App" ,
	data (){
		return {
			isShow : false , 
			num  : 5 , 
			names : ["kia", "mina", "sina"],
			fullnames : [
				{fname : "kia" , lname : "shamaei"},
				{fname : "pari" , lname : "zhd"},
				{fname : "yasi" , lname : "ghami"}
			]
		}

	}

}
</script>

<style>


</style>