<script setup>
import { ref } from 'vue';

let count = ref(0);
</script>

<template>
    <h1>Count: {{ count }}</h1>
    <button v-on:click="count++">Increment</button>
</template>