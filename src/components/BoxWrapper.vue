<template>
    <div>
        <slot></slot>
    </div>
</template>

<script setup>

</script>

<style scoped>
    div {
        background: rgb(56, 56, 56);
        padding: .5em;
        width: 350px;
        display: flex;
        flex-direction: column;
        gap: .5em;
        border-radius: .5em;
    }
</style>