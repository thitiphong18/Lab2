<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import CalComponent from "./components/CalComponent.vue";
import HelloWorldExample from "./components/HelloWorldExample.vue";
import HandingUserInput from "./components/HandingUserInput.vue";
import AtributeBindings from "./components/AtributeBindings.vue";
import ConditionalsAndLoops from "./components/ConditionalsAndLoops.vue";
import FormBindings from "./components/FormBindings.vue";
</script>

<template>
  <div>
    <FormBindings />
    <br /><br />
    <ConditionalsAndLoops />
    <br />
    <br />
    <AtributeBindings />
    <HandingUserInput />
    <CalComponent />
    <HelloWorldExample />
  </div>
</template>

<style scoped></style>
