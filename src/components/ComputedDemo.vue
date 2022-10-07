<script setup>
import { ref } from "vue";
import { computed } from "vue";
let number = ref(9);
let number_squared = computed(() => {
    return number.value * number.value;
});
</script>

<template>
    <h3>Computed Demo</h3>
    <p>Zahl: {{ number }}</p>
    <p>Quadriert: {{ number_squared }}</p>
</template>