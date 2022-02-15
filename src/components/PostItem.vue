<template>
	<div class="post">
	<ul >
		<li><strong>Название :</strong> {{ post.title }}</li>
		<li><strong>Описание :</strong> {{ post.body }}</li>
	</ul>
		<del-btn/>
	</div>
</template>

<script>
    export default {
		    props: {
		        post: {
		            type:Object,
				        required: true
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
		display: flex;
		justify-content: space-between;
		border: 2px solid teal;
	}


</style>