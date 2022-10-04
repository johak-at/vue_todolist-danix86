<script setup>
import { ref } from "vue";
const list = ref([]);
const newItem = ref("");
function add() {
    list.value.push(newItem.value);
    newItem.value = "";
}
function remove(index) {
    list.value.splice(index, 1);
}
</script>

<template>
    <div>
        <h1>TodoList</h1>
        <input v-model="newItem" />
        <button @click="add">Add</button>
        <ul>
            <li v-for="item in list" :key="item">{{ item }}
                <button @click="remove">x</button>
            </li>
        </ul>


    </div>
</template>