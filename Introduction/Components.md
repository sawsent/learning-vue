## What is a component?

Reusable and self contained unit that encapsulates a specific piece of functionality or user interface.

Anything can be a component, from full pages to single divs.

You combine them to create a beautiful website.

Basically, it is the main form of encapsulation, reusability, and modularity in Vue.

## What comprises a component?

1. HTML \<template>\</template>
2. CSS \<style>\</style scoped>
3. JS / TS

the normal way to do it is: 
```vue
<script>

</script>

<template>

</template>

<style scoped>

</style>
```

## Components in components

Well, everything is already a component inside the App component. Basically you need to import it in script setup and then use it as an html element.
```vue
<script setup>
import AnotherComponent from './AnotherComponent.vue'
</script>

<template>
    <AnotherComponent />
</template>
```

## Dynamic data in components

Data can be dynamically added to components with {{ data }}
However, you cant declare variables inside {{ const a = 1; }}

```vue
<script setup>
let message = 'This is a message';

function calculate(n1, n2) {
    return n1 + n2;
}
</script>

<template>
    <h1>{{ message }}</h1>
    <h2>{{ calculate(2, 2) }}</h2>
</template>
```

## Attribute binding 

Simply writing ':' before an atrtibute will make it so that whatwever is inside the "" is javascript:

```vue
<script setup>
const link = 'https://www.twitch.tv/sawsent';
const image ='https://variety.com/wp-content/uploads/2019/09/twitch_logo.jpg?w=1000&h=667&crop=1&resize=1000%2C667'
</script>

<template>
	<a :href="link"> <p> Follow my twitch channel :D </p> </a>
	<img :src="image">
</template>
```

## Dynamic binding

This will bind the entirety of attributes through a js object:

```vue
<script setup>
const imageInfo = {
    src: 'https://variety.com/wp-content/uploads/2019/09/twitch_logo.jpg?w=1000&h=667&crop=1&resize=1000%2C667',
    alt: 'Just a random img',
    width: 400,
    height: 400,
}
</script>

<template>
    <img v-bind:="imageInfo">
</template>
```

## Styling components

You can have global style, local style, and module style, also you can combine them.

### Global Style

```vue
<style>
h1 {
	color: red;
}
</style>
```

### Local Style

```vue
<style scoped>
h1 {
	color: red;
}
</style>
```

### Module Style 

```vue
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
```
