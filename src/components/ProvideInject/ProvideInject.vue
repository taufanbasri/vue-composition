<script setup>
import { provide, ref } from "vue";
import ChildA from "./ChildA.vue";

const name = ref("Taufan");

provide("username", name);
</script>

<template>
  <h3>Parent component {{ name }}</h3>

  <ChildA />
</template>
