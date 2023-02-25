<template>
  <div>
    <button v-on:click="addLike">Лайк</button>
    <button v-on:click="removeLike">Дизлайк</button>
  </div>
  <div>
    <div>Количество лайков {{ likes }}</div>
    <div>Количество дизлайков {{ dislikes }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      likes: 0,
      dislikes: 0,
    };
  },
  methods: {
    addLike() {
      this.likes += 1;
    },
    removeLike() {
      this.dislikes -= 1;
    },
  },
};
</script>

<style></style>
