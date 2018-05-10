<template>
  <div id="app">
    <div class="wrapper">
      <div class="heading">
        <h1>Vui</h1>
      </div>
    </div>
    <div class="wrapper">
      <vui-button>This is a button</vui-button>
    </div>
    <div class="wrapper">
      <vui-input />
      <vui-button usewith="input">Search</vui-button>
    </div>
    <footer>
      <p></p>
    </footer>
  </div>
</template>

<script>
import VuiButton from "./components/VuiButton";
import VuiInput from "./components/VuiInput";

export default {
  name: "app",
  components: {
    VuiButton,
    VuiInput
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
}
</style>
