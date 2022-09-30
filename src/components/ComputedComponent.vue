<script setup>
import { computed, reactive, toRefs } from "vue";

const person = reactive({
  fName: "",
  lName: "",
});

const { fName, lName } = toRefs(person);

const fullName = computed(() => `${person.fName} ${person.lName}`);
</script>

<template>
  <div>
    <h2>Fullname {{ fullName }}</h2>
    <input v-model="fName" type="text" placeholder="First Name" />
    <input v-model="lName" type="text" placeholder="Last Name" />
  </div>
</template>
