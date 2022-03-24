<template>
<div class="index">
  <h1>About Box Office Bits</h1>
  <p>Welcome to Box Office Bits! The ultimate movie lover's online guide.</p>
  <p>Whether you are looking for a new title to fall in love with, or curious how others feel about the newest releases, you have come to the right place!</p>
  <h2>What to Watch</h2>

  <!-- 2 column grid layout, grabbing data from components watch1 and watch2 -->
  <div class="row">
    <div class="col-lg">
      <watch1 />
    </div>
    <div class="col-lg">
      <watch2 />
    </div>
  </div>
</div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<script scoped>

// import components watch1 and watch2
import watch1 from '~/components/whatToWatch1.vue'
import watch2 from '~/components/whatToWatch2.vue'

export default {
  name: 'boxOfficeBits',
  components: {
    watch1,
    watch2
  }
}
</script>


<style lang="scss" scoped>



</style>
