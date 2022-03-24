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
  name: 'watch1',
  data() {
    return {
      show: false,
      msg: 'Click the button above to learn more about the film!',
      fact: "Joaquin Phoenix ad-libbed his scream of 'Am I not merciful?' Connie Nielsen wasn't expecting it, and her frightened reaction was genuine.",
      name: 'Gladiator (2000)',
      about: 'A former Roman General sets out to exact vengeance against the corrupt emperor who murdered his family and sent him into slavery.',
      hook: 'This one is a classic! Epic action scenes in the colosseum, romance, betrayal, need I say more?'
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
