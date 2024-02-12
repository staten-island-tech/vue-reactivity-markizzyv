<template>
    <div>
      <h1>{{ Vinyl.name }}</h1>
      <img :src="Vinyl.img" alt="" />
      <h2>{{ clicked }}</h2>
      <button @click="increment">Click ME</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  const props = defineProps({
    Vinyl: Object,
  });
  //clicker logic
  const clicked = ref(0);
  function increment() {
    clicked.value++;
  }
  </script>
  
  <style scoped>
  img {
    width: 250px;
    height: 300px;
    object-fit: cover;
  }

  </style>

<!--div id= home
    div class= product, cart
    page = cart or product
    v-if :page = cart 
    v-if :page = product

-->