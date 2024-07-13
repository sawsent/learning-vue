<script setup>
import { ref } from 'vue';

let name = ref('');
let email = ref('');
let password = ref('');

</script>

<template>
    <form @submit.prevent="$emit('formSubmit', name, email, password)">
        <input type="text" v-model="name" placeholder="name">
        <input type="text" v-model="email" placeholder="name">
        <input type="text" v-model="password" placeholder="name">
        <button type="submit"> submit </button>
    </form>
</template>

<style scoped>
button {
    width: 100px;
}
</style>