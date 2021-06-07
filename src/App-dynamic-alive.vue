<template>
	<div>
<button v-on:click="isActive = 'TabA'">tabA</button>
<button  v-on:click="isActive = 'TabB'">tabB</button>
<button v-on:click="isActive = 'TabC' ">tabC</button>


<!-- without dynamice component -->

<!-- <TabA v-if="isActive === 'TabA'"/>
<TabB v-if="isActive === 'TabB'"/>
<TabC v-if="isActive === 'TabC'"/> -->

<!--with dynamic component -->
<!-- <component v-bind:is='isActive' /> -->

<!-- dynamic component with keep-alive to save data state in component -->
<keep-alive>
	<component v-bind:is="isActive" />
</keep-alive>


	</div>
</template>

<script>
import TabA from './components/DynamicsComponent/TabA'
import TabB from './components/DynamicsComponent/TabB'
import TabC from './components/DynamicsComponent/TabC'

	export default {
		name : 'App',
		data(){
			return  {
				isActive : 'TabA'
			}
		},
		components : {
			TabA,
			TabB,
			TabC,
		}

	}
</script>

<style lang="scss" scoped>

</style>
