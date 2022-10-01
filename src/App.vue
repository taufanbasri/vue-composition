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

  <card-component>
    <template v-slot:header>
      <h3>Header</h3>
    </template>
    <template v-slot:default>
      <img src="https://picsum.photos/200" alt="image" />
    </template>
    <template v-slot:footer>
      <button>View Details</button>
    </template>
  </card-component>
</template>
