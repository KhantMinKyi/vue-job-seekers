<script setup>
import jobData from "@/jobs.json";
import { ref, defineProps } from "vue";
import JobListing from "./JobListing.vue";
import { RouterLink } from "vue-router";
const jobs = ref(jobData);
console.log(jobs.value);
defineProps({
  limit: Number,
  showButtom: {
    type: Boolean,
    default: false,
  },
});
</script>
<template>
  <section class="bg-gray-50 px-4 py-10">
    <div class="container-xl lg:container m-auto">
      <h2 class="text-3xl font-bold text-cyan-500 mb-6 text-center">
        Browse Jobs
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Jobs  -->
        <JobListing
          v-for="job in jobs.slice(0, limit || jobs.length)"
          :key="job.id"
          :job="job"
        />
      </div>
    </div>
  </section>
  <section v-if="showButtom" class="m-auto max-w-lg my-10 px-6">
    <RouterLink
      to="/jobs"
      class="block bg-black text-white text-center py-4 px-6 rounded-xl hover:bg-gray-700"
      >View All Jobs</RouterLink
    >
  </section>
</template>
