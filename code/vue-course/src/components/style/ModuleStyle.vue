<template>
    <h1 :class="$style['kabab-case-class']">using kabab-case with $ syntax</h1>
    <h1 :class="$style.camelCaseClass">using camelCase and $ syntax</h1>
</template>

<style module>
.kabab-case-class {
    background: firebrick;
    color: white;
}

.camelCaseClass {
    background: darkslategray;
    color: aliceblue;
}
</style>