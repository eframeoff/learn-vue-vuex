<template>
  <div>
    <h3>Список постов</h3>
    <post-item
      @remove="$emit('remove', post)"
      v-for="post in posts"
      v-bind:post="post"
      :key="post.id"
    />
  </div>
</template>

<script>
import PostItem from "@/components/PostItem";

export default {
  components: {
    PostItem,
  },
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
