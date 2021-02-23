<template>
  <div id="app">
    <Pets/>
  </div>
</template>

<script>
import Pets from './components/Pets.vue'

export default {
  name: 'App',
  components: {
    Pets
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
