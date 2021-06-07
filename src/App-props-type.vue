<template>
	<div>
		<Greet name="kia" heroName = "batman"/>
		<Greet name="kami" heroName = "superman" />
		<Greet name="kam" heroName = "vonder woman"/>
		<Greet v-bind:name="name" v-bind:heroName = "channel"/>
		<PropType title="kiadfgdfgdfgfdgfdgfd" comment='goodvue' :like="14"  :isPublish="true" id="kiabala"/>

	</div>
</template>


<script>
import Greet from './components/Greet'
import PropType from './components/PropType'


export default ({
	name : "App",
	components : {
		Greet, PropType
	},
	data(){
		return {
			name : "vishwas",
			channel : "code valuation"
		}
	}
})
</script>
 <style scoped>
 
 </style>