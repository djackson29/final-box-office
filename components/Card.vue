<script>
export default {
  props: {
    movie: Object
  }
}
</script>

<template>
<!-- card component, returning 4 data points from OMDB API: title, year, poster, and imdbID -->
<div class="card">
  <h2 class="card__title">{{ movie.Title }}</h2>
  <p class="card__copy">{{ movie.Year }}</p>
  <img id="motw-img" :src="movie.Poster" class="img-fluid">
  <p class="card__copy"> <a v-bind:href="'https://www.imdb.com/title/'+movie.imdbID" target="_blank">More information about <em><strong>{{ movie.Title }}</strong></em> on IMDB</a></p>
  <hr class="body-hr">
</div>
</template>


<!-- styling for card component and images -->
<style lang="scss" scoped>
.card {
  background-color: #E0E8F9;
  border: none;
  &__title {
    margin-left: 20px;
  }
  &__copy {
    margin-left: 20px;
  }
}
#motw-img {
  max-width: 150px;
  margin-left: 20px;
}

</style>
