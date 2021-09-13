<template>
  <img alt="Vue logo" src="./assets/logo.png"/>
  <BaseButton @onClick="alertOnClick">+</BaseButton>
</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'
import BaseButton from "./components/BaseButton.vue";

export default {
  components: {
    BaseButton,
    HelloWorld,
    TheHeader
  },
  methods: {
    alertOnClick: () => {
      alert('Hello World')
    }
  }
}
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
