<script setup>
import { reactive, toRefs } from "vue";

const person = reactive({
  fName: "",
  lName: "",
});

const { fName, lName } = toRefs(person);
</script>

<template>
  <div>
    <h2>{{ fName }} {{ lName }}</h2>
    <input v-model="fName" type="text" placeholder="First Name" />
    <input v-model="lName" type="text" placeholder="Last Name" />
  </div>
</template>
