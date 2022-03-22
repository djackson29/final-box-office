<script>
export default {
  props: {
    movie: String
  }
}
</script>

<template>
<div class="card">
  <h2 class="card__title">{{ movie.title }}</h2>
  <p class="card__copy">{{ movie.genre }}</p>
  <p class="card__copy">{{ movie.plot }}</p>
  <p class="card__copy">{{ movie.rated }}</p>
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
