<script setup>
import { computed } from "vue";

const props = defineProps({
  firstName: String,
  lastName: String,
});

const fullName = computed(() => {
  return `${props.firstName} ${props.lastName}`;
});
</script>

<template>
  <div>Hello {{ fullName }}</div>
</template>
