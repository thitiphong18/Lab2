<script setup lang="ts">
import { ref } from "vue";
const text = ref("Edit Me");
const checked = ref(true);
const checkedNames = ref(["Jack"]);
</script>

<template>
  <h2>Text Input</h2>
  <input v-model="text" /> {{ text }}

  <h2>Checkbox</h2>
  <input type="checkbox" v-model="checked" id="checkbox" />
  <label for="checkbox">Checked {{ checked }}</label>

  <h2>Multiply Checkbox</h2>
  <input type="checkbox" v-model="checkedNames" id="jack" value="Jack" />
  <label for="jack">Jack</label>
  <input type="checkbox" v-model="checkedNames" id="john" value="John" />
  <label for="john">John</label>
  <input type="checkbox" v-model="checkedNames" id="mike" value="Mike" />
  <label for="mike">Mike</label>
  <p>Check names</p>
  <pre> {{ checkedNames }} </pre>
</template>

<style scoped></style>
