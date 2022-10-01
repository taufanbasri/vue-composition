<script setup>
import {
  onBeforeMount,
  onBeforeUnmount,
  onBeforeUpdate,
  onMounted,
  onUnmounted,
  onUpdated,
} from "vue";

onBeforeMount(() => {
  console.log("LifeCycle onBeforeMount()");
});

onMounted(() => {
  console.log("LifeCycle onMounted()");
});

onBeforeUpdate(() => {
  console.log("LifeCycle onBeforeUpdate()");
});

onUpdated(() => {
  console.log("LifeCycle onUpdated()");
});

onBeforeUnmount(() => {
  console.log("LifeCycle onBeforeUnmount()");
});

onUnmounted(() => {
  console.log("LifeCycle onUnmounted()");
});
</script>

<template>
  <div>Composition API Lifecycle Hooks</div>
</template>
