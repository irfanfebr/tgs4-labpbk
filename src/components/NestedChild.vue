<template>
    <div>
      <h3>Nested Child Component</h3>
      <button @click="sendData('Data from Grandchild Component')">Send Data</button>
      <button @click="sendData('Data from child component:')">Reset Data</button>
    </div>
  </template>
  
  <script setup>
  const emit = defineEmits(['sendData']);
  
  const sendData = (message) => {
    emit('sendData', message);
  }
  </script>
  