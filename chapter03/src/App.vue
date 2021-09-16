<template>
  <img alt="Vue logo" src="./assets/logo.png"/>
  <div>{{ count }}</div>
  <BaseButton @onClick="plusOne">+</BaseButton>
  <BaseButton @onClick="minusOne">-</BaseButton>
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
  data() {
    return {
      count: 0 as number,
    }
  },
  methods: {
    plusOne(): void {
      this.count++
    },
    minusOne(): void {
      this.count--
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
