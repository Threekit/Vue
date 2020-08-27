<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Viewer v-bind:initParams="initParams" />
  </div>
</template>

<script>
import Viewer from "./components/Viewer.vue";

export default {
  name: "App",
  components: {
    Viewer,
  },
  data() {
    return {
      initParams: {
        assetId: "406bd3c3-f3b4-4af9-9b5f-64e69cfbdd3f",
        authToken: process.env.VUE_APP_THREEKIT_AUTH_TOKEN,
        showAR: true,
        showConfigurator: true,
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
