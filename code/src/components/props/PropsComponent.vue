<script setup>
import StaticPropsComponent from './StaticPropsComponent.vue';
import DynamicPropsComponent from './DynamicPropsComponent.vue';
import ChangingPropsValues from './ChangingPropsValues.vue';
import BasicPropValidation from './BasicPropValidation.vue';
import AdvancedPropValidation from './AdvancedPropValidation.vue';

import { ref } from 'vue';

// DynamicPropsComponent
let firstName = ref('Vicente');
let lastName = ref('Figueiredo');

// Changing Props
const myFavoriteNumber = ref(9);


</script>

<template>
    <div class="part">
        <StaticPropsComponent name="Vicente" />
    </div>
    <div class="part">
        <p>Parent</p>
        <div id="form">
            <input type="text" v-model="firstName" placeholder="First Name">
            <input type="text" v-model="lastName" placeholder="Last Name">
        </div>
        <div id="child">
            <p>Child</p>
            <DynamicPropsComponent :firstName="firstName" :lastName="lastName" />
        </div>
    </div>
    <div class="part">
        <ChangingPropsValues :favNum="myFavoriteNumber" />
    </div>
    <div class="part">
        <BasicPropValidation :id="1" :name="20" :age="'string'" />
        <BasicPropValidation :id="2" :name="'Vicente'" :age="21" />
    </div>
    <div class="part">
        <AdvancedPropValidation :id="3" :age="21" />
        <AdvancedPropValidation :age="21" />
        <AdvancedPropValidation :id="10" :name="'vicente'" />
        <AdvancedPropValidation :name="'Vicente'" :age="21" />
    </div>
   
</template>
