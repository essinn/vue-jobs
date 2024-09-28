<script setup lang="ts">
import { RouterLink } from "vue-router";
</script>

<template>
  <section class="py-10">
    <div class="flex items-center justify-center">
      <RouterLink
        to="/jobs"
        class="bg-black text-white text-center py-4 px-6 rounded-md hover:opacity-90"
      >
        Show All Jobs
      </RouterLink>
    </div>
  </section>
</template>
