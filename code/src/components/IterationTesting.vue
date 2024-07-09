<script setup>
    import { ref } from 'vue';

    const defaultList = ['s_sr01', 's_sr02', 's_sr03', 's_sr04', 's_sr05', 's_sr06'];
    
    const myList = ref([...defaultList]);

    const removeFromHand = (element) => {
        const idx = myList.value.indexOf(element);
        myList.value.splice(idx, 1);
    }

    const reset = () => {
        myList.value = [...defaultList];
    }

    const anObject = {
        id: 0,
        someProp: "hi there",
        nested: {
            rela: "asinfA"
        },
        aFinalProp: ["im", "an", "arr", "of", "strings"]
    };

    let cardList = ref(true);
    let objectIter = ref(false);

    const showCardList = () => {
        objectIter.value = false;
        cardList.value = true;
    }

    const showObjectIter = () => {
        objectIter.value = true;
        cardList.value = false;
    }


</script>

<template>

    <div id="selector">
        <button @:click="showCardList()">card list</button>
        <button @:click="showObjectIter()">object iter</button>
    </div>

    <div v-if="cardList">
        <div id="hand">
            <div @:click="removeFromHand(element)" class="card" v-for="element in myList" :key="element">{{ element }}</div>
        </div>
        <button @:click="reset()">reset</button>
    </div>

    <div v-if="objectIter">
        <div>
            object: {{ anObject }}
        </div>
        <p v-for="(value, key) in anObject" :key="key">
	        {{ key }} »»»» {{ value }}
        </p>
    </div>
    
</template>

<style scoped>

#hand {
    display: flex;
    flex-direction: column;
    border: 2px solid red;
    padding: 10px;
    border-radius: 15px;
    width: 50%;
    gap: 5px;
}

.card {
    border: 1px solid black;
    border-radius: 5px;
    padding: 5px;
}

.card:hover {
    background-color: aliceblue;
}

#selector {
    padding: 10px;
    width: 50%;
    display: flex;
    justify-content: space-around;
    border: 2px solid blue;
    border-radius: 15px;
    margin-bottom: 20px;
}

</style>