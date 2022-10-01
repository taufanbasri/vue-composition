<script setup>
import { computed } from "vue";

const props = defineProps({
  firstName: String,
  lastName: String,
});

const fullName = computed(() => {
  return `${props.firstName} ${props.lastName}`;
});

const emit = defineEmits(["callHeroes"]);

const sendEvent = () => {
  return emit("callHeroes", fullName.value);
};
</script>

<template>
  <div>Hello {{ fullName }}</div>
  <button @click="sendEvent">Call Heroes</button>
</template>
