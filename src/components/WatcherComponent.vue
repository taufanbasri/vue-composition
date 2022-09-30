<script setup>
import { reactive, ref, toRefs, watch } from "vue";

const state = reactive({
  firstName: "",
  lastName: "",
});

const { firstName, lastName } = toRefs(state);

// to watch all in state
// watch(state, (newValue, oldValue) => {
//   console.log("firstName Old value", oldValue.firstName);
//   console.log("firstName New value", newValue.firstName);

//   console.log("lastName Old value", oldValue.lastName);
//   console.log("lastName New value", newValue.lastName);
// });

// to watch single element in reactive object
watch(
  () => state.firstName,
  (newValue, oldValue) => {
    console.log("firstName Old value", oldValue);
    console.log("firstName New value", newValue);
  }
);

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
    <div>
      <input
        type="text"
        placeholder="Reactive First Name"
        v-model="firstName"
      />
      <input type="text" placeholder="Reactive Last Name" v-model="lastName" />
    </div>

    <div>
      <input type="text" placeholder="First Name" v-model="fName" />
      <input type="text" placeholder="Last Name" v-model="lName" />
    </div>
  </div>
</template>
