<template>
  <header>
    <div class="logo">
      <img src="../assets/img/logo-spotify.png" alt="Spotify Logo">
    </div>
    <Search 
      @sendSearch="sendGenre"
    />
  </header>
</template>

<script>

import Search from './Search.vue';

export default {
  name: 'Header',
  components: {Search},
  
  methods:{
    sendGenre(genreToPrint){
      console.log(genreToPrint);
      this.$emit('sendGenre', genreToPrint)
    }
  }
}
</script>

<style lang="scss">
  @import '../assets/style/vars.scss';

  header {
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;
    background-color: $primary-color;
    .logo{
      width: 80px;
      img {
        width: 100%;
      }
    }
  }
</style>