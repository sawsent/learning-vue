<script setup>
import IterationTesting from './components/IterationTesting.vue';
import ModelComponent from './components/ModelComponent.vue';
import ComponentsComponent from './components/_01_Components/ComponentsComponent.vue';
import EventsComponent from './components/_02_Events/EventsComponent.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import { ref } from 'vue';

let currentlyShowing = ref("Components");
const myLearnedShit = [
	"Components",
	"Events",
	"Conditional Rendering",
	"Iteration",
	"Model",
	
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
