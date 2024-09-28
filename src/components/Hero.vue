<script setup>
defineProps({
  title: {
    type: String,
    default: "Become a Vue Dev",
  },
  description: {
    type: String,
    default: "Find the vue job that fits your skills and needs",
  },
});
</script>

<template>
  <div class="bg-green-700 max-w-7xl mx-auto py-20 mb-4 px-4 sm:px-6 lg:px-8">
    <div class="flex flex-col items-center text-center">
      <h1 class="text-4xl font-semibold text-white sm:text-5xl md:text-6xl">
        {{ title }}
      </h1>
      <p class="my-5 text-lg md:text-xl text-white">
        {{ description }}
      </p>
    </div>
  </div>
</template>
