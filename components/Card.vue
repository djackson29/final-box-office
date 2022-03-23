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
  <p class="card__copy">{{ movie.Rated }} | {{ movie.Genre }}</p>
  <p class="card__copy">{{ movie.Plot }}</p>
  <img id="motw-img" src="http://img.omdbapi.com/?i=tt1201607&apikey=d36f6554" class="img-fluid">
  <!-- <h2 class="card__title">{{ movie.name.common }}</h2> -->
  <!-- <p class="card__copy">{{ movie.subregion }}</p> -->

</div>
</template>



<style lang="scss" scoped>
.card {
  margin: 10px 0;
  // padding: 10px 0;
  &__title {
    font-size: 1.5rem;
    padding: 20px 10px 0 10px;
  }
  &__copy {
    padding: 0 10px;
  }
}
#motw-img {
  max-width: 150px;
}

</style>
