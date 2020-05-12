<template>
  <div id="app">
    <CkeditorNuxt v-model="content"/>

  </div>
</template>

<script>
import CkeditorNuxt from './components/CkeditorNuxt.vue'

export default {
  name: 'App',
  components: {
    CkeditorNuxt
  },
  data() {
    return {
      content: ''
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
