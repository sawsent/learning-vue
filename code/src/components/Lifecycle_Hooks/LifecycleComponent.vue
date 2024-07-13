<script setup>
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted } from 'vue';

const defaultMessage = 'default message';
const updatedMessage = 'updated message';
const message = ref(defaultMessage);

onBeforeMount(() => {
    console.log('Component is ABOUT to be mounted');
})
onMounted(() => {
    console.log('Component has JUST been mounted');
})
onBeforeUpdate(() => {
    console.log('Component is ABOUT to be updated');
})
onUpdated(() => {
    console.log('Component has JUST been updated');
})
onBeforeUnmount(() => {
    console.log('Component is ABOUT to be unmounted');
})
onUnmounted(() => {
    console.log('Component has JUST been unmounted');
})
</script>

<template>
<h3>Current Message: {{ message }}</h3>
<div style="display: flex; gap: 15px">
    <button @click="message = updatedMessage">Update Message</button>
    <button @click="message = defaultMessage">Reset Message</button>
</div>
</template>