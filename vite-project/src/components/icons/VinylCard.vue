<template>
    <div>
      <h1>{{ Vinyl.name }}</h1>
      <img :src="Vinyl.img" alt="" />
      <h2>{{ clicked }}</h2>
      <h3>{{ Vinyl.price }}</h3>
      
<button @click="addToCart">Add To Cart</button>
      <button @click="secondinc">Press to Play!</button>
    </div>
  </template>
  
  <script setup>
import { defineProps, defineEmits } from "vue";

const props = defineProps({
  Vinyl: Object,
});

const emit = defineEmits(["addToCart"]);

const addToCart = () => {
  emit("addToCart", props.Vinyl); 
  clicked.value++; 
};



</script>
  
  <style scoped>
  img {
    width: 250px;
    height: 300px;
    object-fit: cover;
  }

  button {
    display: flex;
    justify-content: center;
    margin: 10px
   
  }

  </style>

<!--div id= home
    div class= product, cart
    page = cart or product
    v-if :page = cart 
    v-if :page = product

-->