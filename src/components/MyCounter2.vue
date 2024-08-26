<template>
    <div>
      <h1>Counter 2</h1>
      <p>Counter: {{ count }}</p>
      <button @click="start">Increment</button>
    </div>
</template>
  
<script setup>
  import { customRef } from 'vue';

  const count = customRef((track, trigger) => {
    let count = 0;

    return {
      get() {
        track();
        return count;
      },
      set(value) {
        count = value;
        trigger();
      }
    }
  });

  function increment() {
    console.log("Before Increment");
    count.value++;
    console.log("After Increment");
  }
  
</script>
  
  <style scoped>
  </style>