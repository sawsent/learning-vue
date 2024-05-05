## Reactivity

The framework can automatically update the UI whenever data changes.

We can do it with either *reactive()* or *ref()*

Now that component is a reactive component.

```vue
<script setup>
import { ref } from 'vue';

let count = ref(0);
</script>

<template>
    <h1>Count: {{ count }}</h1>
    <button v-on:click="count++">Increment</button>
    <button @:click="count--">Decrement</button>
</template>
```

If you want to access the actual value of count inside the \<script>, then you can use count.value to do so.

```vue
<script setup>
import { ref } from 'vue';

let count = ref(0);

const incrementCounter = () => {
	count.value++;
}

const decrementCounter = () => {
	count.value--;
}

</script>

<template>
    <h1>Count: {{ count }}</h1>
    <button v-on:click="incrementCounter">Increment</button>
    <button @:click="decrementCounter">Decrement</button>
</template>
```

## Passing arguments into functions

You can simply add parameters to events by passing them into the v-on:click. 
```vue
<script setup>

const textAttributes = {
    type: 'text',
    placeholder: 'please enter your name.'
}

const message = 'This is a const message';

const submitHandler = (e) => {
    e.preventDefault();
    alert('Valid')
}

const showMessage = (m) => alert(m);
</script>

<template>
    <form v-on:submit="submitHandler">
        <input :="textAttributes">
        <button type="submit">Submit</button>
    </form>
  
    <button v-on:click="showMessage(message)">Show message</button>

</template>
```

## reactive():

Provides a reactive object that auto-updates on the UI.
Doesn't work for primitive data types!

```vue
<script setup>
import { reactive } from 'vue';

let obj = reactive({ count: 0, })

const increment = () => obj.count++;
const decrement = () => obj.count--;

</script>

<template>
    <h1>Count: {{ obj.count }}</h1>
    <button v-on:click="increment">+</button>
    <button v-on:click="decrement">-</button>
</template>
```

## ref():

Especially design to create a reactive single value.

## Using reactive + ref

You can have a bunch of **ref()** singular elements inside for example a **reactive()** array:

```vue
<script setup>
import { reactive, ref } from 'vue';

let friends = reactive([ref('tuna'), ref('zé'), ref('hortelao')]);
</script>

<template>
	<h1> {{ friends[0] }} </h1>
</template>
```

## Computed properties

It's a special variable that automatically updates when data it depends on also changes. It's liek a little woorker that watches certain data, and updates itself if that data changes.

```vue
<script setup>

import { ref, computed } from 'vue';

const number = ref(5);
const squared = computed(() => {
    return number.value * number.value;
})

</script>

<template>
    <h1>Original Number: {{ number }}</h1>
    <h1>Squared Number: {{ squared }}</h1>
    <button v-on:click="number = 10">change number!</button>
</template>
```

