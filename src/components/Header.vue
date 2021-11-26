<template>
  <header>
    <div class="logo">
      <img src="../assets/img/logo-spotify.png" alt="Spotify Logo">
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss">
  @import '../assets/style/vars.scss';

  header {
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 15px;
    background-color: $primary-color;
    .logo{
      width: 80px;
      img {
        width: 100%;
      }
    }
  }
</style>