<template>
  <div id="app">
    <div class="wrapper">
      <div class="heading">
        <h1>Vui</h1>
      </div>
    </div>
    <div class="wrapper">
      <div class="btn-wrapper">
        <vui-button>This is a button</vui-button>
      </div>
      <div class="btn-wrapper">
        <vui-button><BoxIcon slot="leftIcon" /> Button with icon</vui-button>
      </div>
    </div>
    <div class="wrapper">
      <vui-input placeholder="Write something" labelText="This is a label">
        <vui-button slot="input-button" text="Search" />
      </vui-input>
    </div>
    <footer>
      <p></p>
    </footer>
  </div>
</template>

<script>
import { BoxIcon } from "vue-feather-icons";
import VuiButton from "./components/VuiButton";
import VuiInput from "./components/VuiInput";

export default {
  name: "app",
  components: {
    VuiButton,
    VuiInput,
    BoxIcon
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size: 16px;
}

.wrapper {
  padding: 32px;
  border-top: 1px solid #eee;
  display: flex;
  width: 440px;
  flex-wrap: wrap;
}

.btn-wrapper {
  display: inline-block;
  margin-left: 8px;
}

label {
  width: 100%;
  text-align: left;
}
</style>
