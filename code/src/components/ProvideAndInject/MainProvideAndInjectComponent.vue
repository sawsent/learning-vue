<script setup>
import SchoolComponent from './SchoolComponent.vue';

import { provide } from 'vue';

provide('studentName', 'Alex');
provide('studentAge', 20);
provide('studentLocation', 'Earth');

</script>

<template>
    <div class="part">
        <SchoolComponent :schoolName="'DSP'"></SchoolComponent>
    </div>

</template>