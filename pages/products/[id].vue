<template>
    <div>
        <div>
            <h1>
                Products {{id}}
            </h1>
        </div>
    </div>
</template>

<script setup>
    const {id} = useRoute().params
</script>

<style scoped></style>