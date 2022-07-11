<template>
  <div class="app">
    <Image title="Story tell" msg="Vertel het verhaal bij de foto's"/>
  </div>
</template>

<script>
import Image from './components/Image.vue'

export default {
  name: 'App',
  components: {
    Image
  }
}
</script>

<style>
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
