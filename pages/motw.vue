<template>
<main class="main">

  <!-- grid row with one column for title of page and API data-->
  <div class="row">
    <div class="col">
      <h1>Movie of the Week</h1>
      <p>This week, we are highlighting the entire epic Harry Potter series.</p>

      <!-- iterate though moviesAPI data if it is present -->
      <div v-if="moviesAPI">
        <card v-for="movie of moviesAPI" v-bind:key="movie.id" :movie="movie" />
      </div>
    </div>
  </div>

</main>
</template>


<script>
// import axios and Card component
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

  // metadata
  head() {
    return {
      title: this.title,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content: 'Movie of the Week page on Box Office Bits. We highlight a different movie each week and reveal fun facts about the film.'
        }
      ]
    }
  },

  // get API data
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
