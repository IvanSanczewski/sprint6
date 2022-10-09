<template>
  <Home />
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: { Home }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

  // {sentence: 'Our hero was surfing the Space when suddenly… he spotted a spaceship!', id: 1},
  // {sentence: 'He felt curious about the spaceship, so he entered in. Once there, he got to a room with two doors.', id: 2},
  // {sentence: 'The hero decided to take the door what would take him home.', id: 3},
  // {sentence: 'But the other heroes were not so lucky whith their choice.', id: 4 }