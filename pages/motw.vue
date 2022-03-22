<template>
  <main class="main">

    <!-- grid row with one column for title of page -->
    <div class="row">
      <div class="col">
        <h2>Movie of the Week Archives</h2>
        <div v-if="countries">
          <card
            v-for="country of countries"
            :key="country.id"
            :country="country"
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
      countries: null,
      errored: false
    }
  },
  mounted () {
  axios
    .get('https://restcountries.com/v3.1/region/europe')
    .then(response => (this.countries = response.data))
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
