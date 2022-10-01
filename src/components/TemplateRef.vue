<script setup>
import { onMounted, ref } from "vue";

const inputRef = ref(null);

onMounted(() => {
  inputRef.value.focus();
});
</script>

<template>
  <div>
    <input type="text" ref="inputRef" />
  </div>
</template>
