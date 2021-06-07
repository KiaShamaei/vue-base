<template>
	<div class="list">
		<h3 v-for="name in names" v-bind:key="name.fname">
			<slot :fname="name.fname" :lname="name.lname"></slot>
		</h3>

	</div>
</template>

<script>
	export default {
		name : "NameList",
		data(){
			return {
				names : [
					{fname :  'kia' , lname : 'shamaei' },
					{fname :  'kami' , lname : 'shamaei1' },
					{fname :  'kam' , lname : 'shamaei2' }

				]
			}
		}
	}
</script>

<style  scoped>
.list{
	border: 1px solid #fdfdfd;
	border-radius: 10px;
	box-shadow: 5px 5px 5px rgba(68, 68, 68, 0.6);
	width: 200px;
	padding: 10px;
	margin: 5px;
}

</style>