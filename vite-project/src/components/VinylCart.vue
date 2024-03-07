<template>
    <div>
        <h2>CART</h2>
        <div v-for="vinyl in cart"
        :key="vinyl.name">
        <h3>{{ vinyl.name }}</h3>
    </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
    
h2{
    display: flex;
    width: 70vw;
    background-color: red;
}
</style>
