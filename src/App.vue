<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    {{total}}
    <div class="row">
      <div class="col-3">
        <counter lable="WAYV" @cc="sum" />
      </div>
      <div class="col-3">
        <counter lable="LOVE" @cc="sum" />
      </div>
      <div class="col-3">
        <counter lable="NCT" @cc="sum" />
      </div>
      <div class="col-3">
        <counter lable="SM" @cc="sum" />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import counter from "@/components/counter";

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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
