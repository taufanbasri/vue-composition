<script setup>
import { onMounted, ref } from "vue";
import axios from "axios";

const posts = ref([]);
const errorMsg = ref("");

onMounted(() => {
  getPosts();
});

const getPosts = () => {
  axios
    .get("https://jsonplaceholder.typicode.com/posts")
    .then((response) => {
      console.log(response);

      posts.value = response.data;
    })
    .catch((error) => {
      console.log(error);
      errorMsg.value = "Error retreiving data";
    });
};
</script>

<template>
  <h3 v-if="errorMsg">{{ errorMsg }}</h3>

  <div v-for="post in posts" :key="post.id">
    <h3>{{ post.id }}. {{ post.title }}</h3>
    <p>{{ post.body }}</p>
    <hr />
  </div>
</template>
