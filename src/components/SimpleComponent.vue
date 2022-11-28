<script setup lang="ts">
import { ref } from "vue";
import TodoItem from "./TodoItem.vue";
const groceryList = ref([
  { id: 0, text: "Vegatable" },
  { id: 1, text: "Cheese" },
  { id: 2, text: "Whatever else humans are supposed to eat" },
]);
</script>

<template>
  <ol>
    <TodoItem v-for="item of groceryList" :key="item.id" :todo="item" />
  </ol>
</template>
