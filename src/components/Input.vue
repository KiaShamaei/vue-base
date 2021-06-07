<template>
  <div>
    <div>
      <input type="text" 
	   :value="valueModel"
	  @input="$emit('update:modelValue' , $event.target.value)"
	    />
    </div>
  </div>
</template>

<script>
export default {
	props : {
		modelValue : String
	}
};
</script>

<style lang="scss" scoped>
</style>