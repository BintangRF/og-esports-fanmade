<script setup>
const isVisible = ref(false);

const toggleVisibility = () => {
  isVisible.value = window.scrollY > 200;
};

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
};

onMounted(() => {
  window.addEventListener("scroll", toggleVisibility);
});

onUnmounted(() => {
  window.removeEventListener("scroll", toggleVisibility);
});
</script>

<template>
  <button
    v-if="isVisible"
    @click="scrollToTop"
    class="fixed bottom-6 right-6 w-12 h-12 flex items-center justify-center bg-custom-accent-primary text-custom-text-primary shadow-lg cursor-pointer transition-all duration-300 hover:scale-110 hover:shadow-[0_0_1px_var(--color-custom-accent-primary)] border-2 border-custom-bg-primary"
  >
    <!-- Ikon Panah ke atas -->
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="w-6 h-6"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      stroke-width="2"
    >
      <path stroke-linecap="round" stroke-linejoin="round" d="M5 15l7-7 7 7" />
    </svg>
  </button>
</template>
