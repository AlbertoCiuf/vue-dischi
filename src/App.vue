<template>
  <div>
    <Header 
      @sendGenre="getGenre"
    />
    <Main :gotGenre="selectedGenre"/>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data(){
    return {
      selectedGenre: 'all'
    }
  },
  methods:{
    getGenre(genre){
      this.selectedGenre = genre;
    }
  }
}
</script>

<style lang="scss">

  @import "./assets/style/generals.scss";

</style>
