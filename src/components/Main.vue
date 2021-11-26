<template>
  <main>
    <div class="container">
      <CardsList />
    </div>
  </main>
</template>

<script>
import CardsList from './CardsList.vue'
export default {  
  name: 'Main',
  components: {
    CardsList
  }
}
</script>

<style lang="scss">
  
  @import '../assets/style/vars.scss';

  main {
    height: calc(100vh - 60px);
    background-color: $bg-color;
    .container {
      width: 70%;
      margin: 0 auto;
    }
  }
</style>