<script setup>
const myChannel = 'https://www.youtube.com/@sawsent'
const image = 'https://variety.com/wp-content/uploads/2019/09/twitch_logo.jpg?w=1000&h=667&crop=1&resize=1000%2C667'
</script>

<template>
    <a :href="myChannel"><h1>My Channel</h1></a>
    <img :src="image">
</template>

<style scoped>

</style>
