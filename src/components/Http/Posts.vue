<template>
	<div>
		<!-- get on event click -->
		<!-- <button v-on:click="getPosts">get post data</button> -->
		<p v-if="errMsg">{{errMsg}}</p>
		<div v-for="post in posts" v-bind:key="post.id">
			<h3>{{post.id}} - {{post.title}}</h3>
			<p>{{post.body}}</p>
			<hr/>
		</div>

	</div>
</template>

<script>
import axios  from 'axios';
	export default {
		name : "Posts",
		created(){
			this.getPosts()
		},
		data(){
			return {
				posts : [],
				errMsg : ""
			}
		},
		methods : {
			getPosts(){
				axios.get('https://jsonplaceholder.typicode.com/posts')
				.then(res=>{
					console.log(res.data)
					this.posts = res.data
				})
				.catch(err=>{
					this.errMsg = err
				})
			}
		}
	}
</script>

<style lang="scss" scoped>

</style>