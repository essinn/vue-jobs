<script setup>
import { RouterLink } from "vue-router";
import Card from "./Card.vue";
</script>

<template>
  <section class="py-4 max-w-6xl mx-auto">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-6 p-4 rounded-lg">
      <Card>
        <h2 class="text-2xl font-bold">Developers</h2>
        <p class="mt-2 mb-4">Browse our Vue jobs and start your career today</p>
        <RouterLink to="/jobs">
          <button
            class="px-3 py-2 bg-black text-white rounded-md hover:bg-opacity-90"
          >
            Browse Jobs
          </button>
        </RouterLink>
      </Card>
      <Card bg="bg-green-100">
        <h2 class="text-2xl font-bold">For Employers</h2>
        <p class="mt-2 mb-4">Use Vue Jobs to advertise your developer jobs</p>
        <RouterLink to="/jobs/add">
          <button
            class="px-3 py-2 bg-green-700 text-white rounded-md hover:bg-opacity-90"
          >
            Add Job
          </button>
        </RouterLink>
      </Card>
    </div>
  </section>
</template>
