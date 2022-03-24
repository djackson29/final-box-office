<script>
export default {
  props: {
    movie: Object
  }
}
</script>

<template>
<div class="card">
  <h2 class="card__title">{{ movie.Title }}</h2>
  <p class="card__copy">{{ movie.Year }}</p>
  <img id="motw-img" :src="movie.Poster" class="img-fluid">
  <p class="card__copy"> <a v-bind:href="'https://www.imdb.com/title/'+movie.imdbID" target="_blank">More information about <em><strong>{{ movie.Title }}</strong></em> on IMDB</a></p>
</div>
</template>



<style lang="scss" scoped>
.card {
  background-color: #E0E8F9;
  border: none;
  &__title {
    font-size: 1.5rem;
    margin-top: 10px;
  }
}
#motw-img {
  max-width: 150px;
}

</style>
