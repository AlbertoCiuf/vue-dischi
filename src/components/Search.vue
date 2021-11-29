<template>
  <div class="search-menu">
    <select name="search-genres" id="searchGenres"
      v-model="genre"
      @change="$emit('sendSearch', genre)"
    >
      <option value="all">Scegli un genere</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Search',
  data(){
    return {
      //di default assegno all come value al v-model, in modo che venga visualizzata la prima opzione, che visualizza tutte le cards
      genre:'all'
    }
  }
}
</script>

<style lang="scss">
  select {
    width: 250px;
    text-align: center;
    padding: 5px 15px;
    font-size: 18px;
  }
</style>