<template>
  <div>
    <form @submit.prevent>
      <input
        v-model="post.title"
        class="input"
        type="text"
        placeholder="Название"
      />
      <input
        v-model="post.body"
        class="input"
        type="text"
        placeholder="Описание"
      />
      <button class="button" @click="createPost">Создать пост</button>
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

.button {
  padding: 5px;
  background-color: lightpink;
  border-radius: 20px;
  margin-top: 10px;
}

.input {
  width: 100%;
  padding: 10px;
  margin-top: 10px;
}
</style>
