<script setup>
import useCounter from "../../composables/useCounter";

const { count, incrementCount } = useCounter();
</script>

<template>
  <div>
    <h2 @mouseover="incrementCount">Hovered {{ count }} times</h2>
  </div>
</template>
