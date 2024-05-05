<script setup>
import { ref } from 'vue';

let count = ref(0);

const incrementCounter = () => {
    count.value++;
}

const decrementCounter = () => {
    count.value--;
}

</script>

<template>
    <h1>Count: {{ count }}</h1>
    <button v-on:click="incrementCounter">Increment</button>
    <button @:click="decrementCounter">Decrement</button>
</template>