<script setup>
import FirstComponent from './FirstComponent.vue';
import AnotherComponent from './AnotherComponent.vue';
import AttributeBinding from './AttributeBinding.vue';
import DynamicBinding from './DynamicBinding.vue';
import GlobalStyle from './style/GlobalStyle.vue';
import LocalStyle from './style/LocalStyle.vue';
import CombinedStyle from './style/CombinedStyle.vue';
import ModuleStyle from './style/ModuleStyle.vue';
</script>

<template>
	<FirstComponent />
	<AnotherComponent />
	<AttributeBinding />
	<DynamicBinding />
	<GlobalStyle />
	<LocalStyle />
	<CombinedStyle />
	<ModuleStyle />
</template>

<style scoped></style>