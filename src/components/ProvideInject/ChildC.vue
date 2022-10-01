<script setup>
import { inject, toRefs } from "vue";

const username = inject("username", "Default Username");

const count = inject("count", 0);
const person = inject("person", {});
const increment = inject("increment");

const { firstName, lastName } = toRefs(person);
</script>

<template>
  <h2>Child C component</h2>
  <h3>Component C username - {{ username }}</h3>

  <h3>Child Component C Count - {{ count }}</h3>
  <h3>Child Component C Person - {{ firstName }} {{ lastName }}</h3>

  <button @click="increment">Increment count from Child C</button>
</template>
