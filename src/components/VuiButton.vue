<template>
  <button class="button" :class="size">
    <slot />
  </button>
</template>

<script>
export default {
  name: "vui-button",
  props: {
    size: {
      type: String,
      validator: function(value) {
        // The value must match one of these strings
        return ["lg", "sm", ""].indexOf(value) !== -1;
      },
      default: ""
    }
  }
};
</script>

<style scoped lang="scss">
@import "../styles/app.scss";

.button {
  padding: $padding-button;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 1px;
  background-color: white;
  border: 1px solid #000;
  border-radius: $border-radius-button;
}
</style>
