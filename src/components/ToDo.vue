<script setup>
const props = defineProps(["name", "id"]);
const emits = defineEmits(["delete"]);
</script>

<template>
  <li>
    {{ name }}
    <button @click="emits('delete', id)">x</button>
  </li>
</template>
