<template>
  <div>
    <p>This is from tab C</p>
	<input type="text" v-model="name" name="name">
  </div>
</template>


<script>
export default {
  name: "TabC",
  data(){
	  return {
		  name : ""
	  }
  }
};
</script>

<style lang="scss" scoped>
</style>