<template>
  <div id="app">
    <domtest></domtest>
    <result :data="resultData"></result>
  </div>
</template>

<script>
import result from './components/Result.vue'
import domtest from './components/DOM-test.vue'

export default {
  name: 'app',
    data() {
      return {
      resultData: [
          { name: 'American alligator', location: 'Southeast United States' },
          { name: 'Chinese alligator', location: 'Eastern China' },
          { name: 'Spectacled caiman', location: 'Central & South America' },
          { name: 'Broad-snouted caiman', location: 'South America' },
          { name: 'Jacaré caiman', location: 'South America' },
          { name: 'Black caiman', location: 'South America' },
        ], 
      }
  },
  components: {
    result,
    domtest
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
  margin-top: 60px;
}
</style>
