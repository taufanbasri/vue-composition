<script setup>
import PortalComponent from "./components/PortalComponent.vue";
</script>

<template>
  <teleport to="#portal-root">
    <portal-component />
  </teleport>
</template>
