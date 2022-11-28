<script setup lang="ts">
import { ref } from "vue";
const text = ref("Edit Me");
const checked = ref(true);
const checkedNames = ref(["Jack"]);
const picked = ref("");
const selected = ref("2");
const MultiSelected = ref(["1"]);
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

  <h2>Radio</h2>
  <input type="radio" id="one" value="One" v-model="picked" />
  <label for="one">one</label>
  <input type="radio" id="two" value="Two" v-model="picked" />
  <label for="two">Two</label><br />
  <span>Picked: {{ picked }}</span>

  <h2>Select</h2>
  <select v-model="selected">
    <option disabled value="">Please select one</option>
    <option value="1">A</option>
    <option value="2">B</option>
    <option value="3">C</option>
  </select>
  <span>Selected {{ selected }}</span>

  <h2>Multiple Select</h2>
  <select v-model="MultiSelected" multiple style="width: 100px">
    <option disabled value="">Please select one</option>
    <option value="1">A</option>
    <option value="2">B</option>
    <option value="3">C</option>
  </select>
  <span>Selected {{ MultiSelected }}</span>
</template>

<style scoped></style>
