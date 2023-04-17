<template>
  <okienko></okienko>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import okienko from './components/okienko.vue';

export default {
  name: 'App',
  components: {
    //HelloWorld,
    okienko,
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
