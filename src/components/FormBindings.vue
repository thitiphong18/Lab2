<script setup lang="ts">
import { ref } from "vue";
const text = ref("Edit Me");
</script>

<template>
  <h2>Text Input</h2>
  <input v-model="text" /> {{ text }}
</template>

<style scoped></style>
