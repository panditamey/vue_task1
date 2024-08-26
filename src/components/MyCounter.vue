<template>
    <div>
      <h1>Counter</h1>
      <p>Counter: {{ count }}</p>
      <button @click="start">Increment</button>
    </div>
</template>
  
<script setup>
  import { ref } from 'vue';
  let time;
  const count = ref(0);
  const increment = () => {
    count.value++;
  }
  const start = () => {
    time = setInterval(increment, 1000);
  }

/*
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated } from 'vue';

  export default {
    name: 'MyCounter' // Updated to a multi-word name
  }
  onBeforeMount(() => { 
    console.log('Before Mount')
  });
  onMounted(() => {
    console.log('Mounted')
  });
  onBeforeUpdate(() => {
    console.log('Before Update')
  });
  onUpdated(() => {
    console.log('Updated')
  });
  onBeforeUnmount(() => {
    console.log('Before Unmount')
  });
  onUnmounted(() => {
    console.log('Unmounted')
  });
*/
</script>
  
  <style scoped>
  </style>