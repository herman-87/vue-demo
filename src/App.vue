<template>
    <HelloWord />
    <p>{{ sentence }}</p>

    <input type="text" v-model="name">
    <input type="text" v-model="age">
</template>

<script setup>
import { watch, ref } from "vue";
import HelloWord from "./components/HelloWorld.vue";

const name = ref('herman');
const age = ref(10);
watch(name, (newValue, oldValue) => {
    console.log(`new value: ${newValue} | old value: ${oldValue}`);
}) 
</script>

<style scoped>
.red{
    color: red;
}
.green{
    color: green;
}
</style>
