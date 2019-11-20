<template>
  <div id="app">
    <Logo />
  </div>
</template>

<script>
import Logo from "./components/Logo.vue";

export default {
  name: "app",
  components: {
    Logo
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
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

  background: url("./assets/desk-bg.jpg") no-repeat center center;
  background-size: cover;
}
</style>
