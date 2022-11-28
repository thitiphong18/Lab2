<script setup lang="ts">
import { ref } from "vue";
const text = ref("Edit Me");
const checked = ref(true);
</script>

<template>
  <h2>Text Input</h2>
  <input v-model="text" /> {{ text }}

  <h2>Checkbox</h2>
  <input type="checkbox" v-model="checked" id="checkbox" />
  <label for="checkbox">Checked {{ checked }}</label>
</template>

<style scoped></style>
