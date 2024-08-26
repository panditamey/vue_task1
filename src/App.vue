<template>
  <h1>From app</h1>
  <MyCounter />
</template>

<script>
import MyCounter from './components/MyCounter.vue';

export default {
  name: 'App',
  components: {
    MyCounter // Updated to match the new component name
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