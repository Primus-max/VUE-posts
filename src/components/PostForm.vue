<template>
	<form @submit.prevent>
		<h1>Добавить пост</h1>
		<form-input
						v-model="post.title"
						type="text"
						placeholder="Название поста"
		/>
		<form-input
						v-model="post.body"
						type="text"
						placeholder="Название поста"
		/>
		<add-btn
						@click="createPost"
		/>
	</form>
</template>

<script>

    export default {

        data() {
            return{
                post: {
                    title: '',
                    body: '',
                }
            }
        },
		    methods: {
            createPost() {
                this.post.id = Date.now()
                this.$emit('create', this.post)
		            this.post = {
				            title: '',
				            body: ''
		            }
            }
        }
    }
</script>

<style scoped>
	form{
		display: flex;
		flex-direction: column;
	}
</style>