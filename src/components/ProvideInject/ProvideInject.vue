<script setup>
import { provide, reactive, ref, toRefs } from "vue";
import ChildA from "./ChildA.vue";

const name = ref("Taufan");

provide("username", name);

const count = ref(0);
const state = reactive({
  firstName: "Evita",
  lastName: "Karlina",
});

const increment = () => count.value++;

provide("count", count);
provide("person", state);
provide("increment", increment);

const { firstName, lastName } = toRefs(state);
</script>

<template>
  <h3>Parent component {{ name }}</h3>
  <h3>Parent component count {{ count }}</h3>
  <h3>Parent component person {{ firstName }} {{ lastName }}</h3>

  <button @click="increment">Increment Count</button>
  <ChildA />
</template>
