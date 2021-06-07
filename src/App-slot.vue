<template>
  <div>
    <Card>
		<h2>This title of card</h2>
		<p>this article ...</p>
	</Card>
	<Card>
		<img src="https://picsum.photos/200" alt="tetx">
	</Card>
	<Card>
		<template v-slot:header>
			<h3>this is from multiple slot</h3>
		</template>
		<img src="https://picsum.photos/200" alt="tetx">
		<template v-slot:footer>
			<p>this footer for multiple slot</p>
		</template>
	</Card>
  </div>
</template>

<script>
import Card from './components/Card/Card.vue'
export default {
  name: "App",
  components : {
	Card
  }
};
</script>

<style lang="scss" scoped>
</style>