<script setup>

let message = 'This is a message';

function calculate(n1, n2) {
    return n1 + n2;
}

</script>

<template>
    <h1>{{ message }}</h1>
    <h2>{{ calculate(2, 2) }}</h2>
</template>