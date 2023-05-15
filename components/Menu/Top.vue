<template>
  <nav class="bg-gray-900 text-white py-5 border-b border-gray-700">
    <div
      class="container flex flex-col sm:flex-row justify-center gap-3 sm:gap-0 sm:justify-between items-center"
    >
      <NuxtLink to="/" class="text-2xl font-medium">Thành Kun's Blog</NuxtLink>
      <ul
        class="flex gap-5 items-center justify-end text-gray-300 hover:text-gray-50"
      >
        <li :class="active === '/' ? 'text-primary-400' : ''">
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li :class="active === '/categories' ? 'text-primary-400' : ''">
          <NuxtLink to="/categories">Categories</NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>
<script lang="ts" setup>
const route = useRoute();
const active = computed(() => {
  return route.path;
});
</script>
