<template>
  <main>
    <div class="container">
      <CardsList :receivedGenre="gotGenre"/>
    </div>
  </main>
</template>

<script>
import CardsList from './CardsList.vue'
export default {  
  name: 'Main',
  components: {
    CardsList
  },
  props:{
    gotGenre: String
  }
}
</script>

<style lang="scss">
  
  @import '../assets/style/vars.scss';

  main {
    min-height: calc(100vh - 60px);
    background-color: $bg-color;
    .container {
      width: 75%;
      margin: 0 auto;
      padding: 80px;
    }
  }
</style>