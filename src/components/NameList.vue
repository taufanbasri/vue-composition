<script setup>
import { reactive } from "vue";

const state = reactive({
  names: [
    { firstName: "Bruce", lastName: "Wayne" },
    { firstName: "Klark", lastName: "Kent" },
    { firstName: "Peter", lastName: "Parker" },
  ],
});
</script>

<template>
  <h3 v-for="name in state.names" :key="name.firstName">
    <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
  </h3>
</template>
