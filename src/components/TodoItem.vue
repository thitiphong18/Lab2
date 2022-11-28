<script setup lang="ts">
export interface Eatable {
  id: number;
  text: string;
}
import type { PropType } from "vue";
const props = defineProps({
  todo: {
    type: Object as PropType<Eatable>,
    required: true,
  },
});
</script>

<template>
  <li>{{ todo.text }}</li>
</template>
