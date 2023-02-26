<template>
  <button class="button">
    <slot> </slot>
  </button>
</template>

<script>
export default {
  name: "my-button",
};
</script>

<style scoped>
.button {
  padding: 5px;
  background-color: rgb(252, 145, 161);
  color: white;
  border: none;
  border-radius: 20px;
}

.button:hover {
  opacity: 0.7;
}
</style>
