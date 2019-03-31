<template>
  <div id="app">
    <main>
      <div class="contain">
        <img class="estellejpg" alt="estelle" src="./assets/estelle.png" width="300">
      </div>
    </main>
  </div>
</template>

<script>
export default {};
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
