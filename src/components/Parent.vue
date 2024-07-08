<template>
    <div>
      <h1>Parent Component</h1>
      <child @sendDataToParent="handleData"></child>
      <p>{{ childData }}</p>
      <slot></slot> <!-- Slot digunakan untuk menampilkan konten tambahan -->
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Child from './Child.vue';
  
  const childData = ref('Data from child component:');
  const handleData = (data) => {
    childData.value = data;
  }
  </script>
  