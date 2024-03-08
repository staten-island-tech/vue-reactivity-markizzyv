<template>
    <div>
      <h2>CART</h2>
    <VinylCard
    v-for="(item, index) in cart"
          :key="index"
          :vinyl="item"
          @addToCart="addItemToCart"
       
    />
   
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import VinylCard from './icons/VinylCard.vue';
  
  const cart = ref([]);
  
  const addItemToCart = (vinyl) => {
  cart.value.push(vinyl);
  console.log('Item added to cart:', vinyl);
  console.log('Cart:', cart.value);
};
</script>
  
<style scoped>
    
h2{
    display: flex;
    width: 70vw;
    background-color: red;
}
</style>


<!-- <template>
    <div class="item">
        <h2>CART</h2>
        <h3>{{ props.Item.name }}</h3>
        <img :src="props.Item.img" alt="" />
        <h4>{{ props.Item.price }}</h4>
        
    <button @click="$emit('addToCart', vinyl)">Add To Cart</button>
    </div>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

const props = defineProps({
    Item: Object,
});

const emit = defineEmits(["addToCart"]);

const addToCart = () => {
    emit("addToCart", props.Item);
};
</script>

<style scoped>
h2 {
    display: flex;
    width: 70vw;
    background-color: red;
}
</style> -->