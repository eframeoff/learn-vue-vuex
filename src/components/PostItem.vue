<template>
  <div class="post">
    <div>
      <div><strong>Название поста: </strong>{{ post.title }}</div>
      <div><strong>Текст поста: </strong>{{ post.body }}</div>
    </div>
    <div class="post-buttons">
      <my-button @click='$emit("remove", post)'>Удалить</my-button>
    </div>
  </div>
</template>

<script>
// import MyButton from "@/components/ui/MyButton.vue";
export default {
  //   components: {
  //     MyButton,
  //   },
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
.post {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
