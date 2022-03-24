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
  <p class="card__copy">{{ movie.Year }} | Type: {{ movie.Type }}</p>
  <!-- <p class="card__copy">{{ movie.Type }}</p> -->
  <img id="motw-img" :src="movie.Poster" class="img-fluid">

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
