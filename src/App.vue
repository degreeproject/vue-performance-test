<template>
  <div id="app">
    <memAlloc></memAlloc>
  </div>
</template>

<script>
// import domtest from './components/DOM-test.vue'
import memAlloc from './components/Mem-Alloc'

export default {
  name: 'app',
    data() {
      return {}
  },
  components: {
    // domtest,
    memAlloc
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
