<script setup>
import { inject } from 'vue';

const studentName = inject('studentName');
const studentAge = inject('studentAge');
const studentLocation = inject('studentLocation');

</script>

<template>
    <p>Name: {{ studentName }},
    Age: {{ studentAge }},
    Loc: {{ studentLocation }}</p>
</template>