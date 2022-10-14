<script setup>
const props = defineProps(["name", "id"]);
const emit = defineEmits(["remove"]);
</script>

<template>
    {{name}}
    <button @click="emit('remove', 'id' )">x</button>
</template>