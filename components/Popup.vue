<template>
    <div class="root">
      <button @click="isOpen = true">Open</button>
      
      <div class="modal" v-if="isOpen">
        <div>
          <h2>Notification</h2>
          <p>Hellooooo</p>
          <button @click="isOpen = false">Close</button>
        </div>
      </div>
    </div>
    
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const isOpen = ref(false)
  </script>
  
  <style>
  .root{
    position: relative;
    
  }
  
  .modal{
    position: absolute;
  }
  </style>