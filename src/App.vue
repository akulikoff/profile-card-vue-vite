<script setup lang="ts">
import TestimonialCard from "./components/TestimonialCard.vue";
const data = {
  fullName: "Sara Dole",
  linkBio: "@saradole",
  summary:
    "I've been searching for high-quality abstract images for my design projects, and I'm thrilled to have found this platform. The variety and depth of creativity are astounding!",
  imageUrl: "/profile-thumbnail.png",
};
</script>

<template>
  <TestimonialCard v-bind="data" />
</template>

<style scoped></style>
