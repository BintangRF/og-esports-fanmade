<template>
  <footer
    class="bg-custom-bg-primary border-t border-t-custom-accent-secondary text-custom-text-primary pt-12 px-6"
  >
    <div class="max-w-7xl mx-auto grid md:grid-cols-4 gap-10">
      <!-- Logo + Tagline -->
      <div class="flex flex-col items-start gap-4 col-span-2">
        <NuxtLink to="/" class="flex items-center gap-3 group">
          <img
            src="/icon.webp"
            alt="OG Esports"
            class="h-14 w-auto transition-transform duration-300 group-hover:scale-110"
          />
          <h1 class="text-2xl font-bold uppercase tracking-wide">OG Esports</h1>
        </NuxtLink>
        <p class="text-sm text-custom-text-tertiary leading-relaxed max-w-md">
          "Dream OG. Stay OG." — A journey of greatness across Dota 2, CS,
          Marvel Rivals, EAFC, and Mobile Legends.
        </p>
      </div>

      <!-- Navigation -->
      <div>
        <h3 class="text-lg font-semibold uppercase tracking-wide mb-4">
          Navigation
        </h3>
        <ul class="flex flex-col gap-2 text-custom-text-tertiary">
          <li>
            <NuxtLink to="/" class="hover:text-custom-accent-primary transition"
              >Home</NuxtLink
            >
          </li>
          <li>
            <NuxtLink
              to="/news"
              class="hover:text-custom-accent-primary transition"
              >News</NuxtLink
            >
          </li>
          <li>
            <NuxtLink
              to="/teams"
              class="hover:text-custom-accent-primary transition"
              >Teams</NuxtLink
            >
          </li>
          <li>
            <NuxtLink
              to="/about"
              class="hover:text-custom-accent-primary transition"
              >About</NuxtLink
            >
          </li>
        </ul>
      </div>

      <!-- Connect -->
      <div>
        <h3 class="text-lg font-semibold uppercase tracking-wide mb-4">
          Connect
        </h3>
        <ul class="flex flex-col gap-2 text-custom-text-tertiary">
          <li>
            <a
              href="https://shop.ogs.gg/"
              target="_blank"
              class="hover:text-custom-accent-primary transition"
              >Official Store</a
            >
          </li>
          <li>
            <a
              href="https://twitter.com/OGesports"
              target="_blank"
              class="hover:text-custom-accent-primary transition"
              >Twitter / X</a
            >
          </li>
          <li>
            <a
              href="https://www.instagram.com/ogesports/"
              target="_blank"
              class="hover:text-custom-accent-primary transition"
              >Instagram</a
            >
          </li>
          <li>
            <a
              href="https://www.youtube.com/ogesports"
              target="_blank"
              class="hover:text-custom-accent-primary transition"
              >YouTube</a
            >
          </li>
          <li>
            <a
              href="https://www.twitch.tv/team/ogesports"
              target="_blank"
              class="hover:text-custom-accent-primary transition"
              >Twitch</a
            >
          </li>
          <li>
            <a
              href="https://discord.gg/ogesports"
              target="_blank"
              class="hover:text-custom-accent-primary transition"
              >Discord</a
            >
          </li>
        </ul>
      </div>
    </div>

    <!-- Divider -->
    <div class="mt-10 border-t border-custom-accent-secondary"></div>

    <!-- Bottom Section -->
    <div
      class="flex flex-col md:flex-row items-center justify-between max-w-7xl mx-auto py-6 gap-6"
    >
      <!-- Copyright -->
      <p class="text-sm text-custom-text-tertiary text-center md:text-left">
        © {{ new Date().getFullYear() }} OG Esports Fanmade. All Rights
        Reserved.
      </p>
    </div>
  </footer>
</template>
