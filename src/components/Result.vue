<script setup>
import { defineProps } from "vue";
import {RouterLink } from "vue-router";

const { quizQuestionLength, numberOfCorrectAnswers } = defineProps([
  "quizQuestionLength",
  "numberOfCorrectAnswers",
]);
</script>

<template>
  <div class="results">
    <p>Your result...</p>
    <h1>{{ numberOfCorrectAnswers }}/{{ quizQuestionLength }}</h1>
    <RouterLink to="/">Back to Homepage</RouterLink>
  </div>
</template>

<style scoped>
.results {
  text-align: center;
  padding: 100px 0;
}

p {
  font-size: 20px;
}

h1 {
  font-size: 80px;
}
</style>
