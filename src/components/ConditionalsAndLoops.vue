<script setup lang="ts">
import { ref } from "vue";
const show = ref(true);
</script>

<template>
  <button @click="show = !show">Toggle List</button>
  <button>Push Number</button>
  <button>Pop number</button>
  <button>Reverse List</button>

  <ul v-if="show">
    <li>1</li>
    <li>2</li>
    <li>3</li>
  </ul>
  <p v-else>Hide List</p>
</template>

<script scoped></script>
