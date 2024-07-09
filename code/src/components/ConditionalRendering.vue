<script setup>
    import { ref } from 'vue';
    let isVisible = ref(true);

    const toggleVisibility = () => {
        isVisible.value = !isVisible.value;
        console.log(isVisible.value)
    }
</script>

<template>
    <p v-show="isVisible">This will show if thigerr</p>
    <button @:click="toggleVisibility">toggle</button>
</template>

