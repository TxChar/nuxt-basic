<template>
    <div class="container">
        <h1>HomePage</h1>
        <img src="/images/shop.svg">
    </div>
</template>

<script setup>
    useHead({
    title: 'HomePage',
    meta: [
        { name: 'description', content: 'My amazing site.' }
    ],
    })
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

img{
    height: 150px;
    width: 150px;
}
</style>