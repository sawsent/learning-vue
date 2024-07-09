<script setup>
import ComputedProperties from './ComputedProperties.vue'
import MyEvent from './MyEvent.vue';
import MyEventWithFunctions from './MyEventWithFunctions.vue';
import PassingEventArguments from './PassingEventArguments.vue';
import ReactiveComponent from './ReactiveComponent.vue';
</script>

<template>
    <div id="container">
        <div ><MyEvent /></div>
        <div ><MyEventWithFunctions /></div>
        <div ><PassingEventArguments /></div>
        <div ><ReactiveComponent /></div>
        <div ><ComputedProperties /></div>
    </div>
</template>

<style scoped>
#container {
    display: flex;
    flex-direction: column;
    gap: 20px;
    padding: 20px;
}
#container div {
    padding: 10px;
    border: 1px solid black;
}

</style>