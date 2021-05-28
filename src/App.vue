<template>
<h1> kia is bala ! {{name}}</h1>
<div v-text="lname"></div> 
<div v-html="camel"></div>
</template>

<script>


export default {
  name: 'App',
 data (){
return {
	name :  "shamae" ,
	lname : "vishvas",
	camel : "<b>kia is good learner</b>"
}
 }

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
</style>
