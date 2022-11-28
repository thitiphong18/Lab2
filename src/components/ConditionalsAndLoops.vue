<script setup lang="ts">
import { ref } from "vue";
const show = ref(true);
const list = ref([1, 2, 3]);
</script>

<template>
  <button @click="show = !show">Toggle List</button>
  <button>Push Number</button>
  <button>Pop number</button>
  <button>Reverse List</button>

  <ul v-if="show">
    <li v-for="(item, index) of list" :key="index">{{ item }}</li>
  </ul>
  <p v-else-if="list.length">List is not empty, but hidden.</p>
  <p v-else>List is empty.</p>
</template>

<script scoped></script>
