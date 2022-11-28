<script setup lang="ts">
import { ref } from "vue";
const message = ref("Hello World!");
</script>

<template>
  <p>
    <span :title="message">
      Hover your over me for second to see my dinamically bound titled!
    </span>
  </p>

  <p class="red">
    <span> This should be red... but click me toggle it. </span>
  </p>

  <p style="color: green">
    <span> This should be red... but click me toggle it. </span>
  </p>
</template>

<style scoped>
.red {
  color: red;
}
</style>
