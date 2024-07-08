<template>
    <div>
      <h2>Child Component</h2>
      <nested-child @sendData="handleData"></nested-child>
    </div>
  </template>
  
  <script setup>
  import NestedChild from './NestedChild.vue';
  import { defineEmits } from 'vue';
  
  const emit = defineEmits(['sendDataToParent']);
  
  const handleData = (data) => {
    emit('sendDataToParent', data);
  }
  </script>
  