<script setup>
import { ref, computed } from 'vue';

const number = ref(5);
const squared = computed(() => {
    return number.value * number.value;
})
</script>

<template>
    <h1>Original Number: {{ number }}</h1>
    <h1>Squared Number: {{ squared }}</h1>
    <button v-on:click="number = 10">change number!</button>
</template>