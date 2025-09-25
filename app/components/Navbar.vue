<script setup>
const isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};

// Navigation links
const navLinks = [
  { name: "Home", to: "/" },
  { name: "News", to: "/news" },
  { name: "Teams", to: "/teams" },
  { name: "About", to: "/about" },
];
</script>

<template>
  <header
    class="py-2 px-12 h-20 bg-custom-bg-primary flex items-center justify-between shadow-lg sticky top-0 z-50"
  >
    <!-- Logo -->
    <NuxtLink to="/" class="flex items-center gap-2 group">
      <img
        src="/icon.webp"
        alt="og esport"
        class="h-auto w-12 transition-transform duration-300 group-hover:scale-110"
      />
    </NuxtLink>

    <!-- Desktop Navigation -->
    <nav
      class="hidden md:flex items-center gap-8 text-custom-text-primary font-medium uppercase"
    >
      <ul class="flex gap-6 text-sm">
        <li v-for="link in navLinks" :key="link.to">
          <NuxtLink
            :to="link.to"
            class="relative transition-colors duration-300 hover:text-custom-accent-primary after:absolute after:-bottom-1 after:left-0 after:h-[2px] after:w-0 after:bg-custom-accent-primary after:transition-all after:duration-300 hover:after:w-full"
            active-class="text-custom-accent-primary after:w-full"
            exact
          >
            {{ link.name }}
          </NuxtLink>
        </li>
      </ul>

      <!-- Button -->
      <NuxtLink
        to="https://shop.ogs.gg/"
        target="_blank"
        class="group transition-colors duration-300 relative overflow-hidden px-5 py-2.5 bg-custom-bg-primary border-2 border-custom-bg-primary ring-2 ring-custom-accent-primary"
      >
        <span
          class="absolute inset-0 bg-custom-accent-primary transform -translate-x-full group-hover:translate-x-0 transition-transform duration-500 ease-out"
        ></span>
        <span
          class="relative z-10 group-hover:text-custom-text-primary text-base"
        >
          Official Store
        </span>
      </NuxtLink>
    </nav>

    <!-- Burger Button (Mobile) -->
    <button
      class="md:hidden flex flex-col justify-center items-center w-10 h-10 relative z-50 cursor-pointer"
      @click="toggleMenu"
    >
      <span
        class="block h-0.5 w-6 bg-custom-text-primary transform transition duration-300"
        :class="isOpen ? 'rotate-45 translate-y-2' : ''"
      ></span>
      <span
        class="block h-0.5 w-6 bg-custom-text-primary my-1 transition-opacity duration-300"
        :class="isOpen ? 'opacity-0' : 'opacity-100'"
      ></span>
      <span
        class="block h-0.5 w-6 bg-custom-text-primary transform transition duration-300"
        :class="isOpen ? '-rotate-45 -translate-y-1' : ''"
      ></span>
    </button>

    <!-- Mobile Menu -->
    <transition name="slide-fade">
      <nav
        v-if="isOpen"
        class="absolute top-20 left-0 w-full bg-custom-bg-primary flex flex-col items-center gap-6 py-6 shadow-lg md:hidden text-custom-text-primary"
      >
        <ul class="flex gap-6 text-lg uppercase">
          <li v-for="link in navLinks" :key="link.to">
            <NuxtLink
              :to="link.to"
              class="relative transition-colors duration-300 hover:text-custom-accent-primary after:absolute after:-bottom-1 after:left-0 after:h-[2px] after:w-0 after:bg-custom-accent-primary after:transition-all after:duration-300 hover:after:w-full"
              active-class="text-custom-accent-primary after:w-full"
              exact
              @click="isOpen = false"
            >
              {{ link.name }}
            </NuxtLink>
          </li>
        </ul>

        <!-- Button -->
        <NuxtLink
          to="https://shop.ogs.gg/"
          target="_blank"
          class="group transition-colors duration-300 relative overflow-hidden px-5 py-2.5 bg-custom-bg-primary border-2 border-custom-bg-primary ring-2 ring-custom-accent-primary"
        >
          <span
            class="absolute inset-0 bg-custom-accent-primary transform -translate-x-full group-hover:translate-x-0 transition-transform duration-500 ease-out"
          ></span>
          <span class="relative z-10 group-hover:text-custom-text-primary">
            Official Store
          </span>
        </NuxtLink>
      </nav>
    </transition>
  </header>
</template>

<style scoped>
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 0.3s ease;
}
.slide-fade-enter-from,
.slide-fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
