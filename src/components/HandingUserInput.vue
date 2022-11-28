<script setup lang="ts">
import { ref } from "vue";
const message = ref("Hello World!");
function reverseMessage() {
  message.value = message.value.split("").reverse().join("");
}
function notifly() {
  alert("navigation was prevented.");
}
</script>

<template>
  <h1>{{ message }}</h1>
  <button @click="reverseMessage">Reverse message</button>
  <button @click="message += '!'">Append "!"</button>
  <a href="https://vuejs.org" @click.prevent="notifly"
    >A link with e.preventDefault
  </a>
</template>

<style scoped>
button,
a {
  display: block;
  margin-bottom: 1em;
}
</style>
