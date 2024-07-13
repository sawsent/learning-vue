<script setup>
const props = defineProps({
    id: Number,
    name: String,
    age: Number,
})
</script>

<template>
    <h3>Basic Prop Validation {{ props.id }}</h3>
    <p>{{ props }}</p>
</template>