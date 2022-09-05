<template>
  <HelloWorld />
</template>

<script>
import HelloWorld from "./components/CV.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  max-width: 1000px;
  background-color: #ebecf0;
}

body {
  margin-top: 60px;
  display: flex;
  justify-content: center;
}
</style>
