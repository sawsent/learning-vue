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