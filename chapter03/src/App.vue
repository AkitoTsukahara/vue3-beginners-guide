<template>
  <img alt="Vue logo" src="./assets/logo.png"/>
  <div>{{ count }}</div>
  <BaseButton :disabled="hasMaxCount" @onClick="plusOne">+</BaseButton>
  <BaseButton :disabled="hasMinCount" @onClick="minusOne">-</BaseButton>

  <NumberInput v-model.numberOnly="inputCount" max="9999" min="0"></NumberInput>
  <base-button @onClick="insertCount">insert</base-button>
</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'
import BaseButton from './components/BaseButton.vue'
import NumberInput from './components/NumberInput.vue'

export default {
  components: {
    BaseButton,
    HelloWorld,
    TheHeader,
    NumberInput
  },
  data() {
    return {
      count: 0 as number,
      inputCount: 0 as number
    }
  },
  watch: {
    inputCount(value: number) {
      if (value >= 9999) {
        this.inputCount = 9999;
      }

      if (value <= 0) {
        this.inputCount = 0
      }

    }
  },
  computed: {
    hasMaxCount(): boolean {
      return this.count >= 9999
    },
    hasMinCount(): boolean {
      return this.count <= 0
    }
  },
  methods: {
    plusOne(): void {
      this.count++
    },
    minusOne(): void {
      this.count--
    },
    insertCount(): void {
      this.count = this.inputCount
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
