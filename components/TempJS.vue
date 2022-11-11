<template>
    <button @click="myFunction()">Click me!</button>
</template>

<script setup>
const myFunction = () => {
    alert("Hello World!");
}
</script>