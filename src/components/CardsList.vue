<template>

  <div class="wrapper">
    <div class="cards-list" v-if="isLoaded">
      <Card 
        v-for="(card, index) in cardsToPrint"
        :key="`card-n-${index}`"
        :singleCard="card"
      />
    </div>
    <Loader  v-else/>
  </div>

</template>

<script>

import axios from 'axios';

import Card from './Card.vue'
import Loader from './Loader.vue'

export default {
  name:'CardsList',
  components: {
    Card,
    Loader
  },
  mounted(){
    this.callAPI();
  },
  data(){
    return {
      cardsToPrint:[],
      apiURL: 'https://flynn.boolean.careers/exercises/api/array/music',
      isLoaded: false
    }
  },
  methods:{
    callAPI(){
      axios.get(this.apiURL)
      .then( r => {
        this.cardsToPrint = r.data.response;
        this.isLoaded=true;
      })
      .catch( e => {
        console.log(e);
      })
    }
  }
} 
</script>

<style lang="scss">

  @import "../assets/style/vars.scss";

  .cards-list {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  
</style>