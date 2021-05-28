<template>
<h3 v-if="isShow">this test for condition </h3>
<h3 v-if="num === 6">this test for condition </h3>

<h3 v-else-if="num < 5">this test for condition </h3>
<h3 v-if="num === 5">this test for {{num}} </h3>


  
</template>

<script>
export default {
	name : "App" ,
	data (){
		return {
			isShow : true , 
			num  : 5 
		}

	}

}
</script>

<style>

</style>