<script setup>
import { ref } from "vue";

const name = ref("");
</script>

<template>
  <div>Tab C Content {{ name }}</div>
  <input v-model="name" type="text" />
</template>
