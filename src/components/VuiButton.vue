<template>
  <button class="button" :class="`${size} use-with-${usewith}`">
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
    },
    usewith: {
      type: String
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
  transition: all 0.15s ease-in-out;

  &:active {
    transform: translateY(1px);
    color: #aaaaaa;
  }

  &.lg {
    padding: $padding-button-lg;
    font-size: $button-fontsize-lg;
  }

  &.sm {
    padding: $padding-button-sm;
    font-size: $button-fontsize-sm;
  }

  &.use-with-input {
    border-left: 0;
    border-top-left-radius: 0px;
    border-bottom-left-radius: 0px;
    position: relative;
    left: -1px;
  }
}
</style>
