<script setup lang="ts">
import { ref } from "vue";
const groceryList = ref([
  { id: 0, text: "Vegatable" },
  { id: 1, text: "Cheese" },
  { id: 2, text: "Whatever else humans are supposed to eat" },
]);
</script>

<template>
  <ol>
    <li v-for="item of groceryList" :key="item.id">{{ item.text }}</li>
  </ol>
</template>
