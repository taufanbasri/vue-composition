<script setup>
import { inject } from "vue";

const username = inject("username", "Default Username");
</script>

<template>
  <h2>Child C component</h2>
  <h3>Component C username - {{ username }}</h3>
</template>
