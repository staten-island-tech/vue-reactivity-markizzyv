<template>
  <div class = "container">
<VinylCard
      v-for="vinyl in vinyls"
      :key="vinyl.name"
      :Vinyl="vinyl"
      @addToCart="AddItem"
/>
  <div class="cart-container">
  <div v-if="cart.length > 0">
    <h2 class ="text">CART</h2>
  <div v-for= '( vinyl , index) in cart' :key=index>
    <img :src = "vinyl.img" alt="" width="100vw" height="100vw">
    <h4>{{  vinyl.name }}</h4>
    <h5>{{ vinyl.price }}</h5>

  </div>
  </div>
  </div>
  </div>
</template>

<script setup>
import VinylCart from '@/components/VinylCart.vue';
import VinylCard from '@/components/icons/VinylCard.vue';
import { ref } from 'vue';


const vinyls = [
{
    name: "SZA - SOS",
    International: true,
    price: "$35.50",
    img: "https://merchbar.imgix.net/product/61/3507/7635936706732/JUqpdHH4SZA-SOS.png?quality=60&auto=compress,format&w=3840",
  },
  {
    name: "Daniel Caesar - Never Enough",
    International: true,
    price: "$50.00",
    img: "https://shop.danielcaesar.com/cdn/shop/products/NEVERENOUGH2LPVINYL_540x.png?v=1679416157",
  },
  {
    name: "Sampha - Lahai",
    International: true,
    price: "$45.50",
    img: "https://store.sound-merch.com.au/cdn/shop/files/SAMPA-WHITE-VINYL_760x.png?v=1694064104%27",
  },
  {
    name: "Kali Uchis - Red Moon in Venus",
    International: true,
    price: "$30.00",
    img: "https://th.bing.com/th/id/R.2a3ae860773f6e8ab73fe848eef0c4e3?rik=%2bXWi2ZkD9vOHcw&riu=http%3a%2f%2fcdn.shopify.com%2fs%2ffiles%2f1%2f0548%2f6424%2f8961%2fproducts%2fSanstitre-3_c0c07aff-09c8-4372-8aec-a7219d222bbd_grande.png%3fv%3d1674461903&ehk=ASrYhzhYGzFs%2bU76FO4hGxOW1wnv303h%2bG9T1WrHFkA%3d&risl=&pid=ImgRaw&r=0",
  },
  {
    name: "Travis Scott - Utopia",
    International: false,
    price: "$40.50",
    img: "https://shop.travisscott.com/cdn/shop/files/HERO_VINYL_01_UPDATE-_1_1500x.png?v=1690507172",
  },
  {
    name: "beabadoobee - Beatopia",
    International: false,
    price: "$45.50",
    img: "https://th.bing.com/th/id/OIP.5TzMimczhwi6GaTbd8lXvwHaHa?rs=1&pid=ImgDetMain",
  },
  {
    name: "Lil Yachty - Let's Start Here",
    International: true,
    price: "$40.50",
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },
];

const cart = ref([]);
const AddItem = (vinyl) => {
  cart.value.push(vinyl)
};


</script>

<style scoped>
h1 {
  color: red;
}

.container {
  display: flex;
  width: 70vw;
}

.cart-container{
  color: red;
  margin-bottom: 100px;
}
</style>