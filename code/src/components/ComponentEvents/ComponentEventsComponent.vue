<script setup>
import ComponentEvent from './ComponentEvent.vue';
import ComponentEventWithParams from './ComponentEventWithParams.vue';

import { ref } from 'vue';

// ComponentEvent
let count = ref(0);

// with params

let message = ref('No message yet');

const formHandler = (name, email, password) => {
    message.value = `received info! Name: ${name}; email: ${email}; password: ${password}`
}


</script>

<template>
    <div class="part">
        <h1>Count: {{ count }}</h1>
        <div class="child">
            <ComponentEvent @incrementCounter="count++" />
        </div>
    </div>

    <div class="part">
        <div class="child">
            <ComponentEventWithParams @formSubmit="formHandler" />
        </div>

        <p>{{ message }}</p>

    </div>


</template>

<style scoped>


</style>