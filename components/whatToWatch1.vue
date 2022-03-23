<template>
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
