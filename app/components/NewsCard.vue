<script setup>
defineProps({
  news: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div
    class="grid md:grid-cols-2 max-w-6xl gap-8 items-center overflow-hidden shadow-lg bg-custom-bg-secondary"
  >
    <!-- Left: Image -->
    <div class="relative overflow-hidden">
      <img
        :src="news.image"
        :alt="news.title"
        class="w-full h-80 object-cover transition-transform duration-500 hover:scale-105"
      />
      <!-- Category / Division -->
      <div
        class="absolute top-4 left-4 px-4 py-1 bg-custom-accent-primary text-sm font-medium text-white shadow-md"
      >
        {{ news.category }}
      </div>
    </div>

    <!-- Right: Content -->
    <div
      class="flex flex-col justify-center gap-4 text-custom-text-primary p-6"
    >
      <!-- Meta -->
      <p class="text-sm text-gray-400">{{ news.date }}</p>

      <!-- Title -->
      <h2 class="text-2xl font-bold leading-snug">
        {{ news.title }}
      </h2>

      <!-- Excerpt -->
      <p class="text-gray-300 leading-relaxed">
        {{ news.excerpt }}
      </p>

      <!-- Button -->
      <NuxtLink
        :to="`/news/${news.id}`"
        class="mt-4 px-6 py-2 w-fit bg-custom-accent-primary hover:bg-custom-accent-primary/80 text-custom-text-primary font-semibold uppercase tracking-wide transition shadow-md"
      >
        Read More
      </NuxtLink>
    </div>
  </div>
</template>
