<template>
  <div id="app">
    <Disccomp/>
  </div>
</template>

<script>

import Disccomp from './components/Disccomp.vue'

export default {
  name: 'App',
  components: {
    Disccomp
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
