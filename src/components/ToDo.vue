<script setup>
const props = defineProps(["name", "id"]);
const emits = defineEmits(["remove"]);
</script>

<template>
    <li>
        {{name}}
        <button @click="emits('remove', id )">x</button>
    </li>
</template>