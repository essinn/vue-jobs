<script setup>
import Cards from "@/components/Cards.vue";
import Hero from "@/components/Hero.vue";
import JobListings from "@/components/JobListings.vue";
</script>

<template>
  <Hero />
  <Cards />
  <JobListings :limit="3" :showButton="true" />
</template>
