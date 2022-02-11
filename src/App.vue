<template>
  <div>
    <post-form @create="createPost"/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>
  import PostForm from "@/components/PostForm";
  import PostList from "@/components/PostList";
  export default {
    components: {PostForm, PostList},
    data (){
      return{
        title: '',
        body: '',
        posts: [],
      }
    },
    methods:{
      createPost(post){
        this.posts.push(post)
      }
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

</style>
