<template>
  <div class="input-wrapper">
    <label class="input-label" v-if="labelText">{{labelText}}</label>
    <div class="input-button-wrapper">
      <input :type="type" class="input" :placeholder="placeholder">
      <slot name="input-button" />
    </div>
  </div>
</template>

<script>
import VuiButton from "./VuiButton";

export default {
  name: "vui-input",
  components: {
    VuiButton
  },
  props: {
    type: {
      type: String,
      default: "text",
      validator: function(value) {
        return ["text", "number", ""].indexOf(value) !== -1;
      }
    },
    buttonText: {
      type: String
    },
    labelText: {
      type: String
    },
    placeholder: {
      type: String
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

.input-label {
  text-align: left;
  text-transform: uppercase;
  font-size: 12px;
  margin-bottom: 2px;
  letter-spacing: 1px;
  font-weight: bold;
}

.input-wrapper {
  text-align: left;
}

::-webkit-input-placeholder {
  /* Chrome/Opera/Safari */
  font-style: italic;
}
::-moz-placeholder {
  /* Firefox 19+ */
  font-style: italic;
}
:-ms-input-placeholder {
  /* IE 10+ */
  font-style: italic;
}
:-moz-placeholder {
  /* Firefox 18- */
  font-style: italic;
}
</style>

<style>
.input-button-wrapper {
  display: flex;
}
</style>
