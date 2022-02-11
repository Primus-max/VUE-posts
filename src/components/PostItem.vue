<template>
	<ul class="post">
		<li><strong>Название :</strong> {{ post.title }}</li>
		<li><strong>Описание :</strong> {{ post.body }}</li>
	</ul>
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

</style>