<template>
    <div>
      <h1>Current Count: {{ count }}</h1>
      <button @click="incrementCount">Increment</button>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUpdated } from 'vue';
  const count = ref(0);
  
  const incrementCount = () => {
    count.value += 1;
  };
  
  onUpdated(() => {
    document.title = `Count: ${count.value}`;
  });
  
  onMounted(() => {
    document.title = `Count: ${count.value}`;
  });
  </script>
  
  <style scoped>
  </style>
  