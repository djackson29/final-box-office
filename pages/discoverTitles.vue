<template>
  <div class="discoverTitles">
    <h1>Discover New Titles</h1>

    <!-- v-for to iterate through each image array and display movie posters for each genre -->
    <h2>Action</h2>
    <div>
      <img v-for="action in actionPosters" v-bind:key="action.id" v-bind:src="action" alt="" class="img-thumbnail">
    </div>
    <h2>Musicals</h2>
    <div>
      <img v-for="musical in musicalPosters" v-bind:key="musical.id" v-bind:src="musical" alt="" class="img-thumbnail">
    </div>
    <h2>Thrillers</h2>
    <div>
      <img v-for="thriller in thrillerPosters" v-bind:key="thriller.id" v-bind:src="thriller" alt="" class="img-thumbnail">
    </div>
  </div>
</template>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<script scoped>

export default {
  name: 'discoverTitles',
  data () {
    return {

      // 3 arrays, for images in each genre
      actionPosters: [require('../assets/black-panther.jpg'), require('../assets/hunger-games.jpg'), require('../assets/zombieland.jpg')],
      musicalPosters: [require('../assets/greatest-showman.jpg'), require('../assets/hamilton.jpeg'), require('../assets/west-side.jpg')],
      thrillerPosters: [require('../assets/jaws.jpg'), require('../assets/joker.jpeg'), require('../assets/lambs.jpg')]
    }
  }
}

</script>


<style lang="scss">
img {
  margin: 10px 30px 50px 0;
}

</style>
