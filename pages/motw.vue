<template>
  <main class="main">

    <!-- grid row with one column for title of page -->
    <div class="row">
      <div class="col">
        <h2>Movie of the Week Archives</h2>
        <div v-if="moviesAPI">
          <card
            v-for="movie of moviesAPI"
            :key="movie.id"
            :movie="movie"
          />
        </div>
      </div>
    </div>

    <!-- grid row with 3 columns for main content of page -->
    <!-- <div class="row"> -->

      <!-- v-for to iterate through the placeholder array and populate each column with placeholder content -->
      <!-- <div class="col-lg">
        <div v-for="placeholder in placeholderContent" v-bind:key="placeholder.id">
          <p>{{placeholder}}</p>
        </div>
      </div>
      <div class="col-lg">
        <div v-for="placeholder in placeholderContent" v-bind:key="placeholder.id">
          <p>{{placeholder}}</p>
        </div>
      </div>
      <div class="col-lg">
        <div v-for="placeholder in placeholderContent" v-bind:key="placeholder.id">
          <p>{{placeholder}}</p>
        </div>
      </div>
    </div> -->
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
  mounted () {
  axios
    .get('https://www.omdbapi.com/?i=tt1201607&apikey=d36f6554')
    .then(response => (this.moviesAPI = response.data))
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
