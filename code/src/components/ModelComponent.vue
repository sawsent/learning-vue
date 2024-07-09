<script setup>
import { ref } from 'vue';

const formData = ref({username: '', email: '', password: ''});

</script>

<template>
    <form @submit.prevent>
        <input type="text" placeholder="Enter ur name" v-model="formData.username">
        <input type="text" placeholder="Enter ur email" v-model="formData.email">
        <input type="password" placeholder="Enter ur password" v-model="formData.password">
        <button type="submit">submit</button>
    </form>

    <div>
        <p>username: {{ formData.username }}</p>
        <p>email: {{ formData.email }}</p>
        <p>password: {{ formData.password }}</p>
    </div>

</template>