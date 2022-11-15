<script setup>
import { ref } from 'vue'
const randomNumber = ref(0)
const pupils = ["Migei", "Daniel", "Gergö", "Viki", "Patrick", "Stefan", "Elias", "Josef", "Manuel"];
function random() {
    randomNumber.value = Math.floor(Math.random() * 9) + 1;
}
</script>

<template>
    <h1>{{ randomNumber }} {{ pupils[randomNumber] }} {{ pupils[randomNumber].length }}</h1>

    <button @click="random">New Random Number</button>
</template>