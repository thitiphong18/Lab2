<script setup lang="ts">
import { ref } from "vue";
const message = ref("Hello World!");
function reverseMessage() {
  console.log("call reverse message");
}
</script>

<template>
  <h1>{{ message }}</h1>
  <button @click="reverseMessage">Reverse message</button>
  <button @click="message += '!'">Append "!"</button>
  <a href="">A link with e.preventDefault </a>
</template>

<style scoped>
button,
a {
  display: block;
  margin-bottom: 1em;
}
</style>
