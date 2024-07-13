<script setup>
import IterationTesting from './components/IterationTesting.vue';
import ModelComponent from './components/ModelComponent.vue';
import ComponentsComponent from './components/_01_Components/ComponentsComponent.vue';
import EventsComponent from './components/_02_Events/EventsComponent.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import PropsComponent from './components/props/PropsComponent.vue';
import ComponentEventsComponent from './components/ComponentEvents/ComponentEventsComponent.vue'
import MainSlotComponent from './components/Slot/MainSlotComponent.vue';
import MainProvideAndInjectComponent from './components/ProvideAndInject/MainProvideAndInjectComponent.vue';
import MainLifecycleHooksComponent from './components/Lifecycle_Hooks/MainLifecycleHooksComponent.vue';

import { ref } from 'vue';

let currentlyShowing = ref("Components");
const myLearnedShit = [
	"Components",
	"Events",
	"Conditional Rendering",
	"Iteration",
	"Model",
	"Props",
	"Component Events",
	"Slot",
	"Provide & Inject",
	"Lifecycle Hooks",
]

const enable = (element) => currentlyShowing.value = element;

</script>
<template>
	<div id="selector">
		<button v-for="(element, index) in myLearnedShit" :key="index" @:click="enable(element)"> {{ element }} </button>
	</div>
	<IterationTesting v-if="currentlyShowing === 'Iteration'"/>
	<ModelComponent v-if="currentlyShowing === 'Model'"/>
	<ComponentsComponent v-if="currentlyShowing === 'Components'"/>
	<EventsComponent v-if="currentlyShowing === 'Events'" />
	<ConditionalRendering v-if="currentlyShowing === 'Conditional Rendering'" />
	<PropsComponent v-if="currentlyShowing === 'Props'" />
	<ComponentEventsComponent v-if="currentlyShowing === 'Component Events'" />
	<MainSlotComponent v-if="currentlyShowing=== 'Slot'" />
	<MainProvideAndInjectComponent v-if="currentlyShowing === 'Provide & Inject'" />
	<MainLifecycleHooksComponent v-if="currentlyShowing === 'Lifecycle Hooks'" />
</template>

<style scoped>
#selector {
	padding: 20px;
	margin: 50px;
	border: 2px solid green;
	border-radius: 20px;
	display: flex;
	gap: 15px;
}
</style>
<style>
.part {
    border: 2px solid rgb(255, 0, 0);
    border-radius: 20px;
    padding: 15px;
    margin: 10px;
    display: flex;
    flex-direction: column;
    gap: 10px;
}

#child {
    display: flex;
    flex-direction: column;
    border: 1px solid green;
    border-radius: 5px;
    padding: 10px;
}

.child {
    display: flex;
    flex-direction: column;
    border: 1px solid green;
    border-radius: 5px;
    padding: 10px;
}

button {
	max-width: 150px;
	max-height: max-content;
}
</style>
