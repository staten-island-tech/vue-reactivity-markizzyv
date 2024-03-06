<template>
    <div>
        <h2 class="title">CART</h2>
    <div v-for="vinyl in items.cart" :key= "vinyl.name">
        <h3>{{ vinyl.name }}</h3>
        <h4>{{ vinyl.price }}</h4>
    </div>
    </div>
</template>

<script setup>

const items = definteProps({cart:Array})

</script>
 


<style scoped>
title{
    width: 15vw;
}
h2{
    display: flex;
    width: 70vw;
    background-color: red;
}
</style>
