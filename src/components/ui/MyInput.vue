<template>
  <input
    class="input"
    v-bind:value="modelValue"
    v-on:input="updateInput"
    type="text"
  />
</template>

<script>
export default {
  name: "my-input",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
.input {
  width: 100%;
  padding: 10px;
  margin-top: 10px;
}
</style>
