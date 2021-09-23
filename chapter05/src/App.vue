<script lang="ts">
import {defineComponent} from "vue";
import ButtonSample from "./components/buttons/ButtonSample.vue";
import DialogSample from "./components/dialog/DialogSample.vue";

export default defineComponent({
  name: 'App',
  components: {
    ButtonSample,
    DialogSample
  }
});
</script>
<template>
  <ButtonSample/>
  <DialogSample/>
</template>
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
