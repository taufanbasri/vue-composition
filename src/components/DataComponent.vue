<script setup>
import { ref, reactive } from "vue";

const state = reactive({
  firstName: "Azizah",
  lastName: "Arraya",
});

const reactiveGreeting = `Hello my name is ${state.firstName} ${state.lastName}`;

const firstName = ref("Taufan");
firstName.value = "Evita";
console.log(firstName);
</script>

<template>
  <div>Ref - {{ firstName }}</div>
  <div>Reactive - {{ reactiveGreeting }}</div>
  <div>Access state reactive - {{ state.firstName }} {{ state.lastName }}</div>
</template>
