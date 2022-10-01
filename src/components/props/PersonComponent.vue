<script setup>
import { ref } from "vue";
import PersonGreeting from "./PersonGreeting.vue";

const firstName = ref("");
const lastName = ref("");
</script>

<template>
  <div>
    <input type="text" placeholder="First Name" v-model="firstName" />
    <input type="text" placeholder="Last Name" v-model="lastName" />

    <PersonGreeting :firstName="firstName" :lastName="lastName" />
  </div>
</template>
