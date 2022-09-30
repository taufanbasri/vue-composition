<script setup>
import { ref } from "vue";

const firstName = ref("Taufan");
firstName.value = "Evita";
console.log(firstName);
</script>

<template>
  <h2>Compositions - {{ firstName }}</h2>
</template>
