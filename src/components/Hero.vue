<script setup>
import { defineProps } from "vue";
defineProps({
  title: {
    type: String,
    default: "Become a Developer",
  },
  subtitle: {
    type: String,
    default: "Login to View Jobs",
  },
});
</script>
<template>
  <!-- Hero -->
  <section class="bg-cyan-800 py-20 mb-4">
    <div
      class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col items-center"
    >
      <div class="text-center">
        <h1 class="text-4xl font-extrabold text-white sm:text-5xl md:text-6xl">
          Become a
          <span class="animate-pulse text-black"> Developer </span>
        </h1>
        <p
          class="my-4 text-xl text-white transition ease-in-out delay-150 hover:scale-125 cursor-pointer font-mono"
        >
          <span class="text-black">Find</span> the
          <span class="text-black">Job</span> that fits your
          <span class="text-black font-bold">Skill and Needs</span>
        </p>
        <p class="font-mono text-gray-400">
          {{ subtitle }}
        </p>
      </div>
    </div>
  </section>
</template>
