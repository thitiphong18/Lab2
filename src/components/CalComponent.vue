<script lang="ts">
import { reactive, computed } from "vue";
export default {
  setup() {
    const state = reactive({
      num1: "0",
      num2: "0",
      result: 0,
    });
    const result = computed(function () {
      return parseInt(state.num1) + parseInt(state.num2);
    });
    const add = function () {
      state.result = parseInt(state.num1) + parseInt(state.num2);
    };
    return { state, add, result };
  },
};
</script>

<template>
  <div class="card">
    <div>
      <input
        v-model="state.num1"
        type="text"
        ref="num1"
        style="text-align: center; width: 80%"
      />
    </div>
    <div>+</div>
    <div>
      <input
        v-model="state.num2"
        type="text"
        ref="num2"
        style="text-align: center; width: 80%"
      />
    </div>
    <hr />
    <button @click="add" style="width: 80%">=</button>
    <div ref="result">{{ state.num1 }}+{{ state.num2 }} = {{ result }}</div>
  </div>
</template>

<style>
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  width: 200px;
  text-align: center;
}
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.container {
  padding: 2px 16px;
}
</style>
