<script setup></script>

<template>
    <div class="child">
        <slot name="slot1">
            <h3>default content for slot1</h3>
        </slot>
        <slot name="slot2">
            <h3>default content for slot2</h3>
        </slot>
        <slot>
            <h3>default content for default slot</h3>
        </slot>
    </div>
</template>