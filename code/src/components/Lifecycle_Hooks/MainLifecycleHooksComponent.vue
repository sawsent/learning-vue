<script setup>
import LifecycleComponent from './LifecycleComponent.vue';

import { ref } from 'vue';

const mounted = ref(false);

</script>

<template>
<div class="part">
    <div style="display: flex; gap: 20px">
        <h1>Lifecycle Hooks (open console!)</h1>
        <button @click="mounted = !mounted">Toggle child component!</button>
    </div>

    <div class="child" v-if="mounted">
        <LifecycleComponent />
    </div>
    
</div>

</template>
