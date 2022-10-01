<script setup>
import CardComponent from "./components/CardComponent.vue";
</script>

<template>
  <card-component />
  <CardComponent>Card Content 1</CardComponent>
  <CardComponent>
    <h2>Card Content 2</h2>
  </CardComponent>
  <CardComponent>
    <img src="https://picsum.photos/200" alt="image" />
  </CardComponent>
</template>
