<script setup>
import NameList from "./components/NameList.vue";
</script>

<template>
  <name-list>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }} {{ slotProps.lastName }}
    </template>
  </name-list>

  <name-list>
    <template v-slot:default="slotProps">
      {{ slotProps.lastName }}, {{ slotProps.firstName }}
    </template>
  </name-list>

  <name-list>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }}
    </template>
  </name-list>
</template>
