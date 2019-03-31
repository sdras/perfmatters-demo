<template>
  <div id="app">
    <button @click="isShowing = !isShowing">
      <span v-if="isShowing">Estelle doesn't love you :(</span>
      <span v-else>Estelle loves you!</span>
    </button>
    <input v-model="hairColor" type="color" id="hair" name="hair">
    <label for="hair">Hair</label>

    <main>
      <div class="contain">
        <img class="estellejpg" alt="estelle" src="./assets/estelle.png" width="800">
      </div>

      <div class="contain">
        <app-graphic-estelle width="800" :hairColor="hairColor"/>

        <div class="hearts" v-if="isShowing">
          <app-icon-base width="60" height="60" view-box="100" iconColor="crimson">
            <app-icon-heart></app-icon-heart>
          </app-icon-base>

          <app-icon-base
            width="60"
            height="60"
            view-box="100"
            iconColor="crimson"
            style="transform:translateX(45px)"
          >
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
      isShowing: false,
      hairColor: null
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
$basebeige: #f6bd86;

body {
  background: $basebeige;
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
  margin: 0 50px 0 0;
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
  border-radius: 20px;
  transition: all 250ms ease-in-out;
  -webkit-appearance: none;
  -moz-appearance: none;
}

button.hair {
  background: #00467f; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #1c9963,
    #00467f
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #1c9963,
    #00467f
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

button:hover,
button:focus {
  transition: all 300ms ease-in-out;
  box-shadow: 0 5px 10px 0px #79114f9e;
}

button:active {
  box-shadow: none;
}

button:focus {
  outline: 0;
  box-shadow: 0 5px 10px 0px rgba(119, 16, 78, 0.62);
}

input {
  margin-right: 10px;
}

.hearts {
  position: absolute;
  top: 315px;
  left: 305px;
}

main {
  display: flex;
  justify-content: center;
}

.estellejpg {
  margin: 8%;
}
</style>
