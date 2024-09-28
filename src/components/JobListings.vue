<script setup>
import { ref, onMounted, reactive } from "vue";
import JobListing from "./JobListing.vue";
import ShowButton from "./ShowButton.vue";
import axios from "axios";
import PulseLoader from "vue-spinner/src/PulseLoader.vue";

defineProps({
  limit: Number,
  showButton: {
    type: Boolean,
    default: false,
  },
});

const state = reactive({
  jobs: [],
  isLoading: true,
});

onMounted(async () => {
  try {
    const res = await axios.get("/api/jobs");
    state.jobs = res.data;
  } catch (error) {
    console.log("error: ", error);
  } finally {
    state.isLoading = false;
  }
});
</script>

<template>
  <section class="bg-green-50 py-10 px-4">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-3xl font-bold text-green-700 mb-6 text-center">
        Browse Jobs
      </h2>

      <div v-if="state.isLoading" class="text-center text-gray-500 py-6">
        <PulseLoader />
      </div>

      <div v-else class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <JobListing
          v-for="job in state.jobs.slice(0, limit || state.jobs.length)"
          :key="job.id"
          :job="job"
        />
      </div>

      <div v-if="showButton">
        <ShowButton />
      </div>
    </div>
  </section>
</template>
