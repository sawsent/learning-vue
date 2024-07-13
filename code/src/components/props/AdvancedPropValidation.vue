<script setup>
let newid = 0;
const props = defineProps({
    id: {
        type: Number,
        required: false,
        default: 0
    },
    name: {
        type: String,
        required: false,
        default: 'Anonimous'
    },
    age: {
        type: Number,
        required: true,
        validator: (age) => age >= 18 && age <= 45
    },
})
</script>

<template>
    <h3>Advanced Prop Validation {{ props.id }}</h3>
    <p>{{ props }}</p>
</template>