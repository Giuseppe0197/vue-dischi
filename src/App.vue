<template>
  <div id="app">

    <MyHeader :genres="genreList" @changeGenre="startSearch"/>

    <Disccomp :selectedOption="genreSearch" @genresReady="getGenreList"/>
  </div>
</template>

<script>

import Disccomp from './components/Disccomp.vue'
import MyHeader from './components/MyHeader.vue'

export default {
  name: 'App',
  components: {
    Disccomp,
    MyHeader
  },

  data(){
    return {
      genreList: [],

      genreSearch: ""
    }
  },

  methods: {
    getGenreList(allGenre){
      this.genreList = allGenre
    },

    startSearch(genreSearch){
      this.genreSearch = genreSearch
    }
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
