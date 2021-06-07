<template>
	<div class="card">
		<div class="header">
		  <slot name="header"></slot>
		</div>
		<slot></slot>
		<div class="footer">
		  <slot name="footer"></slot>
		</div>
	</div>
</template>

<script>
	export default {
		
	}
</script>

<style scoped>
.card{
	border: 1px solid #fdfdfd;
	border-radius: 10px;
	box-shadow: 5px 5px 5px rgba(68, 68, 68, 0.6);
	width: 200px;
	padding: 10px;
	margin: 5px;
}
</style>