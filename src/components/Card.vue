<template>
    <div class="card">
      <div class="album-img">
        <img :src="singleCard.poster" :alt="singleCard.title">
      </div>
      <div class="album-info">
        <h3 class="title">
          {{singleCard.title}}
        </h3>
        <div class="author">
          {{singleCard.author}}
        </div>
        <div class="year">
          {{singleCard.year}}
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Card',
  props:{
    singleCard: Object
  }
}
</script>

<style lang="scss" scoped>

  @import "../assets/style/vars.scss";
  .card {
    width: calc(100% / 5 - 20px);
    padding: 10px 20px;
    background-color: $primary-color;
    margin: 10px;
    transition: all .3s;
      .album-img img {
        padding-top: 10px;
        width: 100%;
      }
      .album-info {
        padding-top: 15px;
        text-align: center;
        .title {
          text-transform: uppercase;
          color: #fff;
          font-size: 26px;
          padding-bottom: 15px;
        }
        .author {
          font-size: 24px;
        }
        .year {
          font-size: 20px;
          padding-bottom: 50px;
        }
        .author, .year {
          color: #756E6A;
        }
      }

  }
  .card:hover {
    transform: scale(1.05);
    cursor: pointer;
  }


</style>