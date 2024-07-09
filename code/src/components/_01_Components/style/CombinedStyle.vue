<template>
    <h1 class="text-red">Text red class</h1>
    <h2 class="g-1">Another global style</h2>
    <h2 class="l-1">Another local style</h2>
</template>

<style>
.g-1 {
    background-color: fuchsia;
    color: white;
}
</style>

<style scoped>
.l-1 {
    background-color: black;
    color: greenyellow;
}
</style>