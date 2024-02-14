<template>
  <div>
<DestCard
      v-for="vinyl in vinyls"
      :key="vinyls.name"
      :Vinyl="vinyl"
/>
  </div>
</template>

<script setup>
import DestCard from '@/components/icons/DestCard.vue';
const vinyls = [
  {
    name: "Daniel Caesar - Never Enough",
    International: true,
    price: 1300,
    img: "https://shop.danielcaesar.com/cdn/shop/products/NEVERENOUGH2LPVINYL_540x.png?v=1679416157",
  },
  {
    name: "Sampha - Lahai",
    International: true,
    price: 800,
    img: "https://store.sound-merch.com.au/cdn/shop/files/SAMPA-WHITE-VINYL_760x.png?v=1694064104%27",
  },
  {
    name: "Kali Uchis - Red Moon in Venus",
    International: true,
    price: 1200,
    img: "https://th.bing.com/th/id/R.2a3ae860773f6e8ab73fe848eef0c4e3?rik=%2bXWi2ZkD9vOHcw&riu=http%3a%2f%2fcdn.shopify.com%2fs%2ffiles%2f1%2f0548%2f6424%2f8961%2fproducts%2fSanstitre-3_c0c07aff-09c8-4372-8aec-a7219d222bbd_grande.png%3fv%3d1674461903&ehk=ASrYhzhYGzFs%2bU76FO4hGxOW1wnv303h%2bG9T1WrHFkA%3d&risl=&pid=ImgRaw&r=0",
  },
  {
    name: "Hawaiian Vacation",
    International: false,
    price: 900,
    img: "https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1173&q=80&quot;",
  },
  {
    name: "Cascade Mountains",
    International: false,
    price: 400,
    img: "https://images.unsplash.com/photo-1511497584788-876760111969?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1332&q=80&quot;",
  },
  {
    name: "Egyptian Exploration",
    International: true,
    price: 800,
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },
];
</script>

<style scoped>
h1 {
  color: red;
}
</style>