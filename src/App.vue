<template>
  <div id="app">
    <button @click="isShowing = !isShowing">Estelle loves you!</button>
    <img alt="estelle" src="./assets/estelle.png">
    <div v-if="isShowing" class="contain">
      <app-icon-base view-box="100" iconColor="crimson">
        <app-icon-heart></app-icon-heart>
      </app-icon-base>
    </div>
  </div>
</template>

<script>
import AppIconBase from "./components/AppIconBase.vue";
import AppIconHeart from "./components/AppIconHeart.vue";

export default {
  data() {
    return {
      isShowing: false
    };
  },
  components: {
    AppIconBase,
    AppIconHeart
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

.contain {
  position: relative;
}

button {
  display: inline-block;
  border: none;
  padding: 0.75rem 1.5rem;
  margin: 0;
  text-decoration: none;
  background: #0069ed;
  color: #ffffff;
  font-family: "Avenir", sans-serif;
  font-size: 1rem;
  cursor: pointer;
  text-align: center;
  transition: all 250ms ease-in-out;
  -webkit-appearance: none;
  -moz-appearance: none;
}

button:hover,
button:focus {
  background: #0053ba;
  transition: all 300ms ease-in-out;
  border-radius: 1000px;
}

button:focus {
  outline: 1px solid #fff;
  outline-offset: -4px;
}
</style>
