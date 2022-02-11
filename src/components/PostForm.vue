<template>
	<form @submit.prevent>
		<h1>Добавить пост</h1>
		<input v-model="post.title" type="text" placeholder="Название поста" class="input">
		<input v-model="post.body" type="text" placeholder="Название поста" class="input">
		<add-btn @click="createPost"/>
<!--		<button @click="createPost" type="submit" class="btn">Добавить пост</button>-->
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
	.input {
		margin-bottom: 15px;
		width: 100%;
		height: 35px;

		border: 1px solid turquoise;
	}

</style>