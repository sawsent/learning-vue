<script setup>

</script>

<template>
    <button @click="$emit('incrementCounter')">+</button>
</template>

<style scoped>
button {
    width: 30px;
}
</style>