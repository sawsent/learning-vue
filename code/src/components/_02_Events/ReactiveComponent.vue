<script setup>
import { reactive } from 'vue';

let obj = reactive({ count: 0, })

const increment = () => obj.count++;
const decrement = () => obj.count--;

</script>

<template>
    <h1>Count: {{ obj.count }}</h1>
    <button v-on:click="increment">+</button>
    <button v-on:click="decrement">-</button>
</template>