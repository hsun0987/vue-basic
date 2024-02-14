<template>
  <!-- <HelloWorld msg="Hello World"/> -->
  <!-- <FavoriteNation/> -->
  <!-- <EventHandling/> -->
  <Nations/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import FavoriteNation from './components/FavoriteNation.vue';
// import EventHandling from './components/EventHandling.vue';
import Nations from './components/Nations.vue';

export default {
  name: 'App',
  components: {
    // FavoriteNation
    // EventHandling
    Nations
}
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
