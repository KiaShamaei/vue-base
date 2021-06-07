<template>
  <div>
    <h2>This app page</h2>
    <button v-on:click="isShow = true">show popup</button>
    <!-- <Popup v-show="isShow" @close="isShow = false "/> -->
    <Popup v-show="isShow" @close="changShow" />
  </div>
</template>

<script>
import Popup from "./components/Pop";
console.log("app------------")
export default {
  name: "App",
  data() {
    return {
      isShow: false,
    };
  },
  components: { Popup },
  methods : {
	  changShow(second){
		  this.isShow = false;
		  console.log("second parameter" , second)
	  }
  }
};
</script>

<style lang="scss" scoped>
</style>