<script setup>
import { ArrowLeftIcon } from "lucide-react";
import { RouterLink } from "vue-router";
</script>

<template>
  <section>
    <div class="py-6 px-6">
      <RouterLink
        to="/jobs"
        class="text-green-700 hover:opacity-90 flex items-center px-3 py-2"
      >
        <!-- <ArrowLeftIcon class="h-4 w-4 mr-2" /> -->
        Back to Job Listings
      </RouterLink>
    </div>
  </section>
</template>
