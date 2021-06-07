<template>
	<div>
		<NameList>
			<template  v-slot:default="slotProps">
				{{slotProps.lname}} - {{slotProps.fname}}
			</template>
		</NameList>
		<NameList>
			<template  v-slot:default="slotProps">
				{{slotProps.fname}} - {{slotProps.lname}}
			</template>
		</NameList>
		<NameList>
			<template  v-slot:default="slotProps">
				{{slotProps.lname}} 
			</template>
		</NameList>

	</div>
</template>

<script>
import NameList from './components/NameList-props--slot/NameList'
	export default {
		name:'App',
		components :{
			NameList
		}
	}
</script>

<style lang="scss" scoped>

</style>