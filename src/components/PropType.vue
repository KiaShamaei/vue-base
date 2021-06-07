<template>
<!--we should add inheritAttrs to manual set non-props -->
  <div>
    <h2 v-bind="$attrs">this is a article ...</h2>
    <p>{{ title }}</p>
    <p>{{ like }}</p>
    <p>{{ comment }}</p>
	<p>{{isPublish ?"yes" : "no"}}</p>
  </div>
</template>

<script>
export default {
  name: "PropType",

  props: {
    title: String,
    like: Number,
    comment: {
		type: String,
      required: true,
      default: "it is empty ",
    },
	isPublish : Boolean ,

  },
  	inheritAttrs : false
};
</script>

<style lang="scss" scoped>
</style>