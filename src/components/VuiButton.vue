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
      default: "",
      validator: function(value) {
        // The value must match one of these strings
        return ["lg", "sm", ""].indexOf(value) !== -1;
      }
    }
  }
};
</script>

<style scoped lang="scss">
@import "../styles/app.scss";

.button {
  padding: $padding-button;
  font-size: $button-fontsize;
  text-transform: uppercase;
  letter-spacing: 1px;
  background: none;
  border: 1px solid #000;
  border-radius: $border-radius-button;
  cursor: pointer;
  transition: transform 0.15s ease-in-out;

  &:hover,
  &:focus {
    transform: translateY(-2px);
  }

  &:active {
    transform: translateY(0px);
  }

  &.lg {
    padding: $padding-button-lg;
    font-size: $button-fontsize-lg;
  }

  &.sm {
    padding: $padding-button-sm;
    font-size: $button-fontsize-sm;
  }
}
</style>
