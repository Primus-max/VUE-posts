<template>
	<ul class="post" v-for="post in posts">
		<li><strong>Название :</strong> {{ post.title }}</li>
		<li><strong>Описание :</strong> {{ post.body }}</li>
	</ul>
</template>

<script>
    export default {
        props: {
            posts: {
                type: Array,
		            required:true,
            }
        }

    }
</script>

<style scoped>
	ul {
		list-style: none;
	}

	.post{
		margin-top: 15px;
		padding: 15px;
		border: 2px solid teal;
	}
</style>