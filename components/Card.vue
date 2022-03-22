<script>
export default {
  props: {
    movie: Object
  }
}
</script>

<template>
<div class="card">
  <!-- <h2 class="card__title">{{ country.title }}</h2>
  <p class="card__copy">{{ country.genre }}</p>
  <p class="card__copy">{{ country.plot }}</p>
  <p class="card__copy">{{ country.rated }}</p> -->
  <h2 class="card__title">{{ movie.title }}</h2>
  <!-- <p class="card__copy">{{ country.subregion }}</p> -->

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
