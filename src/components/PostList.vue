<template>
	<div>
		<h1>Список постов</h1>
		<post-item
						v-for="post in posts"
						:post="post"
		/>
	</div>
</template>

<script>
	import PostItem from "@/components/PostItem";
    export default {
        components:{PostItem},
        props: {
            posts: {
                type: Array,
		            required:true,
            }
        }

    }
</script>

<style scoped>


</style>