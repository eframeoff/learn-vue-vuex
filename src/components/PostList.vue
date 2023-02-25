<template>
  <div class="post" v-for="post in posts">
    <div><strong>Название поста: </strong>{{ post.title }}</div>
    <div><strong>Текст поста: </strong>{{ post.body }}</div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style>
.post {
  border: 2px solid lightpink;
  padding: 5px;
  margin: 5px;
  border-radius: 20px;
}
</style>
