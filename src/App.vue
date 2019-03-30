<template>
  <div id="app">
    <button @click="isShowing = !isShowing">Estelle loves you!</button>

    <main>
      <div class="contain">
        <img class="estellejpg" alt="estelle" src="./assets/estelle.png" width="600">
      </div>

      <div class="contain">
        <app-graphic-estelle width="600"/>
        <div class="hearts" v-if="isShowing">
          <app-icon-base view-box="100" iconColor="crimson">
            <app-icon-heart></app-icon-heart>
          </app-icon-base>
          <app-icon-base view-box="100" iconColor="crimson">
            <app-icon-heart></app-icon-heart>
          </app-icon-base>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import AppIconBase from "./components/AppIconBase.vue";
import AppIconHeart from "./components/AppIconHeart.vue";
import AppGraphicEstelle from "./components/AppGraphicEstelle.vue";

export default {
  data() {
    return {
      isShowing: false
    };
  },
  components: {
    AppIconBase,
    AppIconHeart,
    AppGraphicEstelle
  }
};
</script>

<style lang="scss">
body {
  background: #f6bd86;
}

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
  background: #ec008c; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #fc6767,
    #ec008c
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #fc6767,
    #ec008c
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
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
  transition: all 300ms ease-in-out;
  border-radius: 20px;
}

button:focus {
  outline: 1px solid #fff;
}

.hearts {
  position: absolute;
}

main {
  display: flex;
  justify-content: center;
}

.estellejpg {
  margin: 8%;
}
</style>
