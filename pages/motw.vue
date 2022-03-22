<template>
<div class="movieWeek">
  <main class="main">

    <!-- grid row with one column for title of page -->
    <div class="row">
      <div class="col">
        <h2>Movie of the Week Archives</h2>
        <!-- <div class="container" v-if="movies">
          <card v-for="movie of moviesAPI" :key="movie.id" :movie="movie" />
        </div> -->
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
</div>
</template>



<script>
// import axios from 'axios'
// import Card from '~/components/Card.vue'

export default {
  name: 'movieWeek'
  // components: {
  //   Card
  // },
  // data() {
  //   return {
  //     loading: true,
  //     moviesAPI: null,
  //     errored: false
  //     array for placeholder content
  //     placeholderContent: [
  //       "<placeholder for API data>",
  //       'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
  //     ]
  //   }
  // },
  // mounted () {
  // axios
  //   .get('http://www.omdbapi.com/?i=tt3896198&apikey=d36f6554')
  //   .then(response => (this.moviesAPI = response.data))
  //   .catch(error => {
  //     console.log(error)
  //     this.errored = true
  //   })
  //   .finally(() => this.loading = false)
  // }
}


// fetch('http://www.omdbapi.com/?i=tt3896198&apikey=d36f6554')
//   .then(data =>
//   data.json()
// )
// .then(data => {
//   console.log(data);
//   document.querySelector('pre').innerHTML = JSON.stringify(data);
// })
// .catch(error => console.error(error));

</script>



<style lang="scss">

</style>
