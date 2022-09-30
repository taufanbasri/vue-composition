<script setup>
import { ref, reactive, toRefs } from "vue";

const state = reactive({
  fName: "Azizah",
  lName: "Arraya",
});

const { fName, lName } = toRefs(state);

const reactiveGreeting = `Hello my name is ${state.firstName} ${state.lastName}`;

const firstName = ref("Taufan");
firstName.value = "Evita";
console.log(firstName);
</script>

<template>
  <div>Ref - {{ firstName }}</div>
  <div>Reactive - {{ reactiveGreeting }}</div>
  <div>Access state reactive - {{ state.firstName }} {{ state.lastName }}</div>
  <div>toRefs - {{ fName }} {{ lName }}</div>
</template>
