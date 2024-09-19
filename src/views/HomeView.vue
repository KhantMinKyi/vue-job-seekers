<script setup>
import Hero from "@/components/Hero.vue";
import HomeCart from "@/components/HomeCart.vue";
import JobListings from "@/components/JobListings.vue";
</script>
<template>
  <Hero subtitle="Hello! Khant Min Kyi" />
  <HomeCart />
  <JobListings :limit="3" :showButtom="true" />
</template>
