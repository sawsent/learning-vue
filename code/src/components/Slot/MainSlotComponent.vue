<script setup>
import SlotComponent from './SlotComponent.vue';
import FallBackContentSlotComponent from './FallBackContentSlotComponent.vue';
import NamedSlotComponent from './NamedSlotComponent.vue'


</script>

<template>
    <div class="part">
        <SlotComponent>
            <h1>Content 1</h1>
            <h2>Content 2</h2>
        </SlotComponent>
    </div>
    <div class="part">
        <h1>Without passing arguments</h1>
        <div class="child">
            <FallBackContentSlotComponent />
        </div>
        
        <h1>With arguments</h1>
        <div class="child">
            <FallBackContentSlotComponent>
                <h2>I passed this as an Argument!</h2>
            </FallBackContentSlotComponent>
        </div>
    </div>

    <div class="part">
        <h2>Passing to both slots</h2>
        <NamedSlotComponent>
            <template v-slot:slot1>
                <h3 class="custom">custom content for slot1</h3>
            </template>
            <template #slot2>
                <h3 class="custom">custom content for slot2</h3>
            </template>
        </NamedSlotComponent>
        <h2>Passing to only slot1</h2>
        <NamedSlotComponent>
            <template #slot1>
                <h3 class="custom">custom content for slot1</h3>
            </template>
        </NamedSlotComponent>
        <h2>Passing to slot1 and default slot with #default</h2>
        <NamedSlotComponent>
            <template #slot1>
                <h3 class="custom">custom content for slot1</h3>
            </template>
            <template #default>
                <h3 class="custom">custom content for default slot</h3>
            </template>
        </NamedSlotComponent>
    </div>
</template>

<style scoped>
.custom {
    color: red;
}
</style>