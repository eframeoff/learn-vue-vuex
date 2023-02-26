<template>
  <div>
    <form @submit.prevent>
      <my-input v-model="post.title" type="text" placeholder="Название" />
      <my-input v-model="post.body" type="text" placeholder="Описание" />
      <my-button style="margin-top: 10px" @click="createPost"
        >Создать пост</my-button
      >
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      const newPost = {
        id: Date.now(),
        title: this.post.title,
        body: this.post.body,
      };
      this.$emit("create", newPost);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>

<style>
form {
  display: flex;
  flex-direction: column;
}
</style>
