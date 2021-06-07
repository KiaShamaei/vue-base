<template>
<Input v-model="name" />

</template>

<script>

import Input from './components/Input.vue'
	export default {
  components: { Input },
		name : "App" ,
		data(){
			return {
				name :  ""
			}
		}
		
	}
</script>

<style lang="scss" scoped>

</style>