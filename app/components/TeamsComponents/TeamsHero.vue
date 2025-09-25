<template>
  <div class="relative w-screen h-[70vh]">
    <!-- Hero Image -->
    <img
      src="/teams.webp"
      alt="hero image"
      class="w-full h-full object-cover object-center"
      draggable="false"
    />

    <!-- Overlay -->
    <div
      class="absolute inset-0 bg-gradient-to-t from-custom-bg-primary/30 via-custom-bg-primary/10 to-transparent pointer-events-none"
    ></div>

    <div
      class="absolute inset-0 bg-gradient-to-r from-custom-bg-primary/30 via-custom-bg-primary/10 to-transparent pointer-events-none"
    ></div>

    <div
      class="absolute inset-0 bg-gradient-to-l from-custom-bg-primary/30 via-custom-bg-primary/10 to-transparent pointer-events-none"
    ></div>
  </div>
</template>
