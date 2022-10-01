<script setup>
import useCounter from "../../composables/useCounter";

const { count, incrementCount } = useCounter(100, 10);
</script>

<template>
  <div>
    <button @click="incrementCount">Clicked {{ count }} times</button>
  </div>
</template>
