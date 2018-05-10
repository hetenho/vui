<template>
  <button :class="`button ${size} use-with-${usewith}`" @click="$emit('click')">
    <div class="button-content">
      <span class="leftIcon">
        <slot name="leftIcon" />
      </span>
      <span>
        <slot /> {{text}}
      </span>
      <span class="rightIcon">
        <slot name="rightIcon" />
      </span>
    </div>
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
    },
    text: {
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
    color: #00000055;
  }

  &.lg {
    padding: $padding-button-lg;
    font-size: $button-fontsize-lg;
  }

  &.sm {
    padding: $padding-button-sm;
    font-size: $button-fontsize-sm;
  }

  .input-button-wrapper & {
    border-left: 0;
    border-top-left-radius: 0px;
    border-bottom-left-radius: 0px;
    position: relative;
    left: -1px;
  }
}

.button-content {
  display: flex;
  justify-content: center;
  align-items: center;
}

.leftIcon {
  margin-right: $pd-sm;
}

.rightIcon {
  margin-left: $pd-sm;
}

button svg {
  width: 12px;
  height: 12px;
  display: flex;
}
</style>
