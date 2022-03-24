<template>
<!-- data and button component for right column of home page -->
<div class="button-component">
  <h3>{{ name }}</h3>
  <p>{{ about }}</p>
  <p>{{ hook }}</p>
  <p><button type="button" name="button" v-on:click="show = !show">Did you Know?</button></p>

  <!-- if button is clicked it will show a fun fact about each movie -->
  <div v-if="show">
    <p>{{ fact }}</p>
  </div>

  <!-- else it shows a message that tells user to click the button -->
  <div v-else>
    <p>{{msg}}</p>
  </div>
</div>
</template>

<script>
export default {
  name: 'watch2',
  data() {
    return {
      show: false,
      msg: 'Click the button above to learn more about the film!',
      name: 'Without a Paddle (2004)',
      about: 'After their friend dies, three men fulfill their childhood dream by going on a camping expedition for the lost D. B. Cooper bounty, with calamitous results.',
      hook: 'Proceed with caution: After watching, you will want to abandon all repsonsibilities and go treasure hunting with friends!',
      fact: 'Most of the outdoor camping scenes were shot inside a very large warehouse.'
    }
  }
}
</script>

<!-- button styling for this component only -->
<style lang="scss" scoped>
button {
  background-color: #647ACB;
  box-shadow: inset 0 3px 0 #98aeeb, 0 1px 1px hsla(0, 0%, 0%, .2);
  border-radius: 10px;
  border: none;
  padding: 1rem 1.5rem;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  cursor: pointer;
  &:hover {
    text-decoration: underline;
    box-shadow: inset 0 2px 2px hsla(0, 0%, 0%, .75), 0 5px 0 hsla(0, 0%, 100%, .15);
  }
}
</style>
