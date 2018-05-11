<template>
  <div id="app">
    <button v-on:click="getDeviceInfo()">Get Device Data</button>
    <p> {{ info }}</p>
  </div>
</template>

<script>
import { Plugins } from "@capacitor/core";
const { Device } = Plugins;

export default {
  name: "App",
  data() {
    return {
      info: null
    };
  },
  methods: {
    async getDeviceInfo() {
      this.info = await Device.getInfo();
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
