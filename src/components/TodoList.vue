<script setup>
import { ref } from "vue";
import { computed } from "vue";
const list = ref([]);
const newItem = ref("");
const filter = ref("");
const filteredList = computed(() => {
    let result = [];
    for (let i = 0; i < list.value.length; i++) {
        if (list.value[i].toLowerCase().includes(filter.value.toLowerCase())) {
            result.push(list.value[i]);
        }
    }
    return result;
});
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
        <input @keyup.enter="add" v-model="newItem" />
        <br /><br />
        <input type="text" placeholder="filter list" v-model="filter" />
        <ul>
            <li v-for="(item, index) in filteredList" :key="item">
                {{index}} - {{item}}
                <button @click="remove(index)">x</button>
            </li>
        </ul>


    </div>
</template>