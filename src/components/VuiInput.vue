<template>
  <input :type="type" class="input">
</template>

<script>
export default {
  name: "vui-input",
  props: {
    type: {
      type: String,
      default: "text",
      validator: function(value) {
        return ["text", "number", ""].indexOf(value) !== -1;
      }
    }
  }
};
</script>

<style scoped lang="scss">
@import "../styles/app.scss";

.input {
  border: 1px solid #000;
  padding: $padding-input;
  border-radius: $border-radius-input;
  font-size: 12px;
}
</style>
