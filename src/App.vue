<template>
  <div id="app">
    <Logo />
    <div class="page-bg"></div>
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
}

.page-bg {
  position: absolute;
  width: 100%;
  height: 100%;
  background: url("./assets/desk-bg.jpg") no-repeat center center;
  background-size: cover;
  animation: fadein 2s;
  z-index: -1;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
