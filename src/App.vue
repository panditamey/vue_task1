<template>
  <h1>From app</h1>
  <MyCounter />
  <MyCounter2 />
</template>

<script>
import MyCounter from './components/MyCounter.vue';
import MyCounter2 from './components/MyCounter2.vue';

export default {
  name: 'App',
  components: {
    MyCounter,
    MyCounter2 // Updated to match the new component name
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