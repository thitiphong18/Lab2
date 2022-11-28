<script setup lang="ts">
import { ref } from "vue";
const message = ref("Hello World!");
const isRed = ref(true);
const color = ref("green");
function togglered() {
  isRed.value = !isRed.value;
}
function toggleColor() {
  color.value = color.value === "green" ? "blue" : "green";
}
</script>

<template>
  <p>
    <span :title="message">
      Hover your over me for second to see my dinamically bound titled!
    </span>
  </p>

  <p :class="{ red: isRed }" @click="togglered">
    <span> This should be red... but click me toggle it. </span>
  </p>

  <p :style="{ color }" @click="toggleColor">
    <span>
      This should be green, and should toggle between green and blue on click.
    </span>
  </p>
</template>

<style scoped>
.red {
  color: red;
}
</style>
