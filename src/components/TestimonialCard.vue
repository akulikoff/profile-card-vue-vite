<script setup lang="ts">
interface CardProps {
  fullName: string;
  linkBio: string;
  summary: string;
  imageUrl: string;
}
defineProps<CardProps>();
</script>

<template>
  <body class="bg-gradient-to-b from-grey-50 to-grey-600">
    <div class="card flex flex-col justify-center px-4 mx-auto">
      <article class="bg-white rounded-lg p-4 shadow-lg">
        <div class="my-4 flex flex-row">
          <img
            :src="imageUrl"
            alt="profile image"
            loading="lazy"
            class="h-12 w-12 rounded-full"
          />
          <div class="flex flex-col ml-4">
            <h3 class="text-lg text-neutral-900 font-semibold line-clamp-1">
              {{ fullName }}
            </h3>
            <span class="text-sm text-neutral-600 font-medium">{{
              linkBio
            }}</span>
          </div>
        </div>
        <p class="text-neutral-600 mb-2 font-medium text-base line-clamp-5">
          {{ summary }}
        </p>
      </article>
    </div>
  </body>
</template>

<style scoped>
body {
  margin: 0;
  font-family: "Noto Sans", sans-serif;
  min-height: 100vh;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-rendering: optimizeLegibility;
}

.card {
  width: 372px;
  margin-top: 200px;
}

* {
  box-sizing: border-box;
}
</style>
