<template>
  <div id="app">
    <div class="wrapper">
      <div class="heading">
        <h1>Vui</h1>
      </div>
    </div>
    <div class="wrapper">
      <vui-button>nope</vui-button>
    </div>
    <footer>
      <p></p>
    </footer>
  </div>
</template>

<script>
import VuiButton from "./components/VuiButton";

export default {
  name: "app",
  components: {
    VuiButton
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
}
</style>
