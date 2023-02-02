<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <p>{{ aGuy.name }}</p>
  <p>{{ aGuy.price }}</p>
  <HelloWorld msg="Hello Vue 3 in CodeSandbox!" />
</template>

<script lang="ts">
import HelloWorldVue from "./components/HelloWorld.vue";
import { Person } from "./types";

export default {
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
  },
  setup() {
    const aGuy: Person = {
      name: "Rafa",
      age: 20,
    };

    return {
      aGuy,
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
