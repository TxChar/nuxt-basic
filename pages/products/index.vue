<template>
    <h1 style="text-align: center;">All Products</h1>
    <div class="container">
        <div v-for="product in data.products">
            <NuxtLink :to="`/products/${product.id}`">
                <h2 class="title">
                    {{ product.title }}
                </h2>
                <img :src=product.thumbnail>
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
    const { data } = await useFetch('https://dummyjson.com/products?limit=12')
    console.log(data)
</script>

<style scoped>
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 5px;
}

.container div{
    width: 300px;
    height: 300px;
    margin: 30px 15px;
    background: #333;
}

.container div:hover{
    background-color: orange;
}

.title {
    color: white;
    text-align: center;
    font-size: 1.2em;
}

/* img {
    height: 200px;
    width: 200px;
} */
</style>