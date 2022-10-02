<script setup>
import { ref } from "vue";

import TabA from "./components/dynamics/TabA.vue";
import TabB from "./components/dynamics/TabB.vue";
import TabC from "./components/dynamics/TabC.vue";

const activeTab = ref(TabA);
</script>

<template>
  <button @click="activeTab = TabA">Tab A</button>
  <button @click="activeTab = TabB">Tab B</button>
  <button @click="activeTab = TabC">Tab C</button>

  <component :is="activeTab"></component>
</template>
