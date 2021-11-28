<template>
  <div id="app">
    <Sidebar></Sidebar>

    <router-view />
  </div>
</template>

<script>
import Sidebar from "./components/sidebar.vue";

export default {
  components: {
    Sidebar,
  },

  data() {
    return {};
  },
  methods: {},
};
</script>

<style>
@font-face {
  font-family: "assistant";
  src: url("./assets/Assistant-VariableFont_wght.ttf");
}

#app {
  font-family: assistant;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: #2c3e50; */
}

body {
  background-color: #2c3e50;
  height: 100vh;
  margin: 0;
}
</style>
