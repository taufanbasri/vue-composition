<script setup>
import { reactive, ref, toRefs } from "vue";

const count = ref(0);
const increment = () => count.value++;

const person = reactive({
  fName: "Taufan",
  lName: "Prasetyo",
});

const changeName = () => {
  person.fName = "Evita";
  person.lName = "Karlina";
}
const { fName, lName } = toRefs(person);
</script>

<template>
  <div>
    <div>
      <h2>{{ count }}</h2>
      <button @click="increment">Increment</button>
    </div>
    <div>
      <h2>{{ fName }} {{ lName }}</h2>
      <button @click="changeName">Change Name</button>
    </div>
  </div>
</template>
