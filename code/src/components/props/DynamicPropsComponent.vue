<script setup>
import { ref } from 'vue';
const props = defineProps(['firstName', 'lastName']);

</script>

<template>
    <p>First Name: {{ props.firstName }}</p>
    <p>Last Name: {{ props.lastName }}</p>
</template>