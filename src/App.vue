<template>
  <div id="app">
    <img alt="estelle" src="./assets/estelle.png">
    <app-icon-demo/>
  </div>
</template>

<script>
import AppIconDemo from "./components/AppIconDemo.vue";

export default {
  components: {
    AppIconDemo
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
