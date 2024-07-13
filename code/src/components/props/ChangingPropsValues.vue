<script setup>
const props = defineProps(['favNum']);
props.favNum = 7; // doesnt work! Check console
</script>

<template>
    <h1>
        {{ props.favNum }}
    </h1>
</template>