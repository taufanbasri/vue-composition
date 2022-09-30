<script setup>
import { ref, watch } from "vue";

const fName = ref("");
const lName = ref("");

watch([fName, lName], (newValues, oldValues) => {
  console.log("fName Old value", oldValues[0]);
  console.log("fName New value", newValues[0]);

  console.log("lName Old value", oldValues[1]);
  console.log("lName New value", newValues[1]);
});
</script>

<template>
  <div>
    <input type="text" placeholder="First Name" v-model="fName" />
    <input type="text" placeholder="Last Name" v-model="lName" />
  </div>
</template>
