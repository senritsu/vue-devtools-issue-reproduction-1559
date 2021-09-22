<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
  <WithGenericProps v-bind="{ foo, bar }" />
  <WithObjectProps v-bind="{ foo, bar }" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import WithGenericProps from "./components/WithGenericProps.vue";
import WithObjectProps from "./components/WithObjectProps.vue";

export default defineComponent({
  name: "App",
  components: {
    HelloWorld,
    WithGenericProps,
    WithObjectProps,
  },
  data() {
    return {
      foo: [{ a: 3, b: true }],
      bar: "baz",
    };
  },
});
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
