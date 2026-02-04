<template>
  <div id="app"></div>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <Exercise1 />
  <Exercise2 />
  <Exercise3 />
  <Exercise4 />
  <Exercise5 />
  <Exercise6 />
</template>

<script>
import Exercise1 from './components/Exercise1.vue';
import Exercise2 from './components/Exercise2.vue';
import Exercise3 from './components/Exercise3.vue';
import Exercise4 from './components/Exercise4.vue';
import Exercise5 from './components/Exercise5.vue';
import Exercise6 from './components/Exercise6.vue';


export default {
  name: 'App',
    components: {
      Exercise1,
      Exercise2,
      Exercise3,
      Exercise4,
      Exercise5,
      Exercise6
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
