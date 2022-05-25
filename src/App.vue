<template>
  <navView />
</template>

<script>
import nav from "../components/navView.vue";

export default {
  name: "App",
  components: {
    navView,
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

img {
  height: 400px;
  width: 400px;
  border-radius: 30px;
}

body {
  height: 100vh;
  background: url(./assets/bgAnniv.png) no-repeat center/cover fixed;
}
</style>
