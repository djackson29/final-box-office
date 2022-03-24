<template>
<main class="main">

  <!-- grid row with one column for title of page and API data-->
  <div class="row">
    <div class="col">
      <h2>Movie of the Week</h2>
      <p>This week, instead of just one movie, we are highlighting the entire epic Harry Potter series.</p>
      <div v-if="moviesAPI">
        <card
          v-for="movie of moviesAPI"
          v-bind:key="movie.id"
          :movie="movie"
        />
      </div>
    </div>
  </div>

</main>
</template>


<script>
import axios from 'axios'
import Card from '~/components/Card.vue'

export default {
  name: 'movieWeek',
  components: {
    Card
  },
  data() {
    return {
      loading: true,
      moviesAPI: null,
      errored: false
    }
  },
  mounted() {
    axios
      .get('https://www.omdbapi.com/?s=harry+potter&apikey=d36f6554')
      .then(response => {
        console.log(response)
        this.moviesAPI = response.data.Search
        console.log(response.data.Search)
      })

      .catch(error => {
        console.log(error)
        this.errored = true
      })
      .finally(() => this.loading = false)
  }
}
</script>



<style lang="scss">

</style>
