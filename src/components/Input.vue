<template>
    <input v-model="inputValue" type="text" >
</template>

<script setup>
const inputValue = defineModel();
</script>

<style scoped>
    input {
        padding: .5em;
        border-radius: .5em;
        border: 2px solid rgba(26, 26, 26, 0.486);
        background: none;
        color: white;
    }
</style>