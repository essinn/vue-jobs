<script setup>
import logo from "@/assets/logo.png";
import { RouterLink, useRoute } from "vue-router";

const isActiveLink = (routePath) => {
  const route = useRoute();
  return route.path === routePath;
};
</script>

<template>
  <div class="bg-green-700 border-b border-green-500">
    <div class="mx-auto max-w-7xl px-2 sm:px-6">
      <div class="flex h-20 items-center justify-center md:justify-between">
        <div class="flex">
          <RouterLink to="/">
            <img :src="logo" alt="logo" class="h-10 w-auto mr-4 md:mr-0" />
          </RouterLink>
        </div>
        <div class="flex gap-4">
          <RouterLink
            :class="[
              isActiveLink('/')
                ? 'bg-green-800 text-white px-2 py-1 rounded'
                : 'text-white text-lg hover:bg-green-800 px-2 py-1 rounded',
            ]"
            to="/"
          >
            Home
          </RouterLink>
          <RouterLink
            :class="[
              isActiveLink('/jobs')
                ? 'bg-green-800 text-white px-2 py-1 rounded'
                : 'text-white text-lg hover:bg-green-800 px-2 py-1 rounded',
            ]"
            to="/jobs"
          >
            Jobs
          </RouterLink>
          <RouterLink
            :class="[
              isActiveLink('/jobs/add')
                ? 'bg-green-800 text-white px-2 py-1 rounded'
                : 'text-white text-lg hover:bg-green-800 px-2 py-1 rounded',
            ]"
            to="/jobs/add"
          >
            Add Jobs
          </RouterLink>
        </div>
      </div>
    </div>
  </div>
</template>
