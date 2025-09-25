<!-- components/TeamsComponents/PlayerCard.vue -->
<script setup>
defineProps({
  nickname: String,
  name: String,
  role: String,
  image: String,
  country: String,
  yearsActive: Number,
  achievements: Number,
  socials: {
    type: Array,
    default: () => [],
  },
});
</script>

<template>
  <div
    class="relative bg-custom-bg-secondary rounded-2xl overflow-hidden shadow-lg border-2 border-custom-accent-secondary transition-all duration-500 group h-[480px] w-[380px]"
  >
    <!-- Foto Player -->
    <div class="relative h-full w-full overflow-hidden flex justify-center">
      <div
        class="absolute inset-0 bg-gradient-to-t from-custom-accent-primary/5 via-custom-accent-secondary/5 to-transparent"
      ></div>
      <img
        :src="image"
        :alt="name"
        class="w-auto h-full object-cover transform group-hover:scale-105 transition-transform duration-700"
      />
    </div>

    <!-- Info Utama -->
    <div
      class="absolute top-5 left-5 w-full text-left text-custom-text-primary uppercase"
    >
      <h3 class="text-3xl font-bold">{{ nickname }}</h3>
      <p class="text-base text-custom-text-secondary">{{ role }}</p>
    </div>

    <!-- Info Tambahan -->
    <div
      class="absolute bottom-0 left-0 w-full bg-custom-bg-secondary text-custom-text-primary p-5 transform translate-y-full group-hover:translate-y-0 transition-all duration-500"
    >
      <h3 class="text-lg font-bold">{{ name }}</h3>
      <p class="text-sm text-custom-text-tertiary">
        {{ role }} • {{ country }}
      </p>

      <div class="flex justify-around mt-4 text-center">
        <div>
          <p class="text-lg font-bold">{{ yearsActive }}+</p>
          <p class="text-xs text-custom-text-tertiary">Years Active</p>
        </div>
        <div>
          <p class="text-lg font-bold">{{ achievements }}</p>
          <p class="text-xs text-custom-text-tertiary">Achievements</p>
        </div>
      </div>
    </div>

    <!-- Sidebar Sosial Media (muncul di kanan) -->
    <div
      class="absolute top-0 right-0 h-full w-0 group-hover:w-16 flex flex-col items-center justify-start pt-5 gap-5 overflow-hidden transition-all duration-500"
    >
      <a
        v-for="s in socials"
        :key="s.name"
        :href="s.url"
        target="_blank"
        rel="noopener noreferrer"
        class="text-custom-text-primary hover:text-custom-accent transition-colors"
      >
        <!-- SVG Sosial Media -->
        <svg
          v-if="s.name === 'twitter'"
          xmlns="http://www.w3.org/2000/svg"
          fill="currentColor"
          viewBox="0 0 24 24"
          class="w-6 h-6"
        >
          <path
            d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 
               4.48 0 0 0-7.86 3v1A10.66 10.66 0 
               0 1 3 4s-4 9 5 13a11.64 11.64 
               0 0 1-7 2c9 5 20 0 20-11.5a4.5 
               4.5 0 0 0-.08-.83A7.72 7.72 
               0 0 0 23 3z"
          />
        </svg>

        <svg
          v-else-if="s.name === 'instagram'"
          xmlns="http://www.w3.org/2000/svg"
          fill="currentColor"
          viewBox="0 0 24 24"
          class="w-6 h-6"
        >
          <path
            d="M7 2C4.2 2 2 4.2 2 7v10c0 2.8 
               2.2 5 5 5h10c2.8 0 5-2.2 
               5-5V7c0-2.8-2.2-5-5-5H7zm10 
               2c1.7 0 3 1.3 3 
               3v10c0 1.7-1.3 3-3 
               3H7c-1.7 0-3-1.3-3-3V7c0-1.7 
               1.3-3 3-3h10zm-5 3a5 
               5 0 1 0 0 10 5 5 0 0 0 
               0-10zm0 2a3 3 0 1 1 0 
               6 3 3 0 0 1 0-6zm4.5-2.9a1.1 
               1.1 0 1 0 0 2.2 1.1 
               1.1 0 0 0 0-2.2z"
          />
        </svg>

        <svg
          v-else-if="s.name === 'youtube'"
          xmlns="http://www.w3.org/2000/svg"
          fill="currentColor"
          viewBox="0 0 24 24"
          class="w-6 h-6"
        >
          <path
            d="M10 15l5.19-3L10 9v6zm12-3c0 
               2.5-.2 4.1-.5 5.1-.3 1-1 
               1.8-2 2.1C18.5 19.8 12 
               20 12 20s-6-.2-7.5-.8c-1-.3-1.7-1.1-2-2.1C2 
               16.1 2 14.5 2 12s.2-4.1.5-5.1c.3-1 
               1-1.8 2-2.1C5.5 4.2 12 4 12 
               4s6 .2 7.5.8c1 .3 1.7 1.1 2 
               2.1.3 1 .5 2.6.5 5.1z"
          />
        </svg>
      </a>
    </div>
  </div>
</template>
