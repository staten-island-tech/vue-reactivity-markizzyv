<template>
  <div>
    <h1>{{ Vinyl.name }}</h1>
    <img :src="Vinyl.img" alt="" />
    <h2>{{ clicked }}</h2>
    <h3>{{ Vinyl.price }}</h3>
    
    <button @click="addToCart">Add To Cart</button>
  </div>
</template>

<script setup>
import { ref, defineProps, defineEmits } from "vue";

const props = defineProps({
  Vinyl: Object,
});

const emit = defineEmits(["addToCart"]);

const clicked = ref(0);

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

