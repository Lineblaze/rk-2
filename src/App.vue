<template>
  <Header_main />
  <Main />
  <Footer_main />
</template>

<script>
import Header_main from "./components/Header_main.vue";
import Main from "./components/Main.vue";
import Footer_main from "./components/Footer_main.vue";

export default {
  name: "App",
  components: {
    Header_main,
    Main,
    Footer_main,
  },
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
