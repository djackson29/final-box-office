<script>
export default {
  props: {
    movie: Array
    // Title: String,
    // Genre: String,
    // Plot: String,
    // Rated: String
  }
}
</script>

<template>
<div class="card">
  <h2 class="card__title">{{ movie.Title }}</h2>
  <p class="card__copy">{{ movie.Rated }} | {{ movie.Genre }}</p>
  <p class="card__copy">{{ movie.Plot }}</p>
  <!-- <h2 class="card__title">{{ movie.name.common }}</h2> -->
  <!-- <p class="card__copy">{{ movie.subregion }}</p> -->

</div>
</template>



<style lang="scss" scoped>
.card {
  border: 1px solid black;
  border-radius: 0;
  margin: 10px 0;
  &__title {
    font-size: 1.5rem;
  }
  &__copy {

  }
}

</style>
