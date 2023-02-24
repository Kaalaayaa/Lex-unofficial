<template>
  <NavBar />
  <HeroBanner />
</template>

<script>
import NavBar from "./components/NavBar.vue";
import HeroBanner from "./components/HeroBanner.vue";

export default {
  name: "App",
  components: {
    NavBar,
    HeroBanner
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #f7f5f2;
}
</style>
