<script setup>
import { RouterLink, useRoute } from "vue-router";
import logo from "@/assets/img/logo.png";

const isActive = (routePath) => {
  const route = useRoute();
  return route.path === routePath;
};
</script>
<template>
  <nav class="bg-slate-600 border-b border-slate-600 fixed w-full z-10">
    <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
      <div class="flex h-20 items-center justify-between">
        <div
          class="flex flex-1 items-center justify-center md:items-stretch md:justify-start"
        >
          <!-- Logo -->
          <RouterLink class="flex flex-shrink-0 items-center mr-4" to="/">
            <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
            <span class="hidden md:block text-white text-2xl font-bold ml-2"
              >Jobs Seekers</span
            >
          </RouterLink>
          <div class="md:ml-auto">
            <div class="flex space-x-2">
              <RouterLink
                to="/"
                :class="[
                  isActive('/')
                    ? 'text-cyan-500 border-cyan-800 bg-cyan-800 border hover:bg-cyan-900 hover:text-white'
                    : 'hover:border hover:border-cyan-500',
                  'text-white',
                  ' px-3',
                  'py-2',
                  ' rounded-md ',
                ]"
                >Home</RouterLink
              >
              <RouterLink
                to="/jobs"
                :class="[
                  isActive('/jobs')
                    ? 'text-cyan-500 border-cyan-800 bg-cyan-800 border hover:bg-cyan-900 hover:text-white'
                    : 'hover:border hover:border-cyan-500',
                  'text-white',
                  ' px-3',
                  'py-2',
                  ' rounded-md ',
                ]"
                >Jobs</RouterLink
              >
              <RouterLink
                to="/jobs/add"
                :class="[
                  isActive('/jobs/add')
                    ? 'text-cyan-500 border-cyan-800 bg-cyan-800 border hover:bg-cyan-900 hover:text-white'
                    : 'hover:border hover:border-cyan-500',
                  'text-white',
                  ' px-3',
                  'py-2',
                  ' rounded-md ',
                ]"
                >Add Job</RouterLink
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
