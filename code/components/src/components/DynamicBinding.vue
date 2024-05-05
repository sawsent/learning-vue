<script setup>
const imageInfo = {
    src: 'https://variety.com/wp-content/uploads/2019/09/twitch_logo.jpg?w=1000&h=667&crop=1&resize=1000%2C667',
    alt: 'Just a random img',
    width: 400,
    height: 400,
}
</script>

<template>
    <img v-bind:="imageInfo">
</template>