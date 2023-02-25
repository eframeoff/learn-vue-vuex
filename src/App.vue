<template>
  <div>
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {
    PostForm,
    PostList,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "JS 1", body: "Какое то описание поста" },
        { id: 2, title: "JS 2", body: "Какое то описание поста" },
        { id: 3, title: "JS 3", body: "Какое то описание поста" },
        { id: 4, title: "JS 4", body: "Какое то описание поста" },
        { id: 5, title: "JS 5", body: "Какое то описание поста" },
      ],
      title: "",
      body: "",
    };
  },
  methods: {
    createPost(newPost) {
      this.posts.push(newPost);
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
