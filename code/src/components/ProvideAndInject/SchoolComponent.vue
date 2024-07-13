<script setup>
import StudentComponent from './StudentComponent.vue';

defineProps(['schoolName']);

</script>

<template>
    <h1>Students in School {{ schoolName }}</h1>
    <StudentComponent />
</template>