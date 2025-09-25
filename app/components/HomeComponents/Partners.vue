<script setup>
const partners = [
  {
    id: 1,
    logo: "/partners/red_bull.webp",
    name: "red bull",
    src: "https://www.redbull.com",
  },
  {
    id: 2,
    logo: "/partners/og-token.webp",
    name: "og fan token",
    src: "https://www.fantokens.com/trade/og-fan-token",
  },
  {
    id: 3,
    logo: "/partners/SCAN_3XS.webp",
    name: "scan 3xs",
    src: "https://scan.co.uk/",
  },
  {
    id: 4,
    logo: "/partners/secret_lab.webp",
    name: "secret lab",
    src: "https://secretlab.co/",
  },
];
</script>

<template>
  <section class="py-16">
    <h2 class="text-center text-xl font-semibold text-custom-text-primary mb-8">
      Our Partners
    </h2>

    <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-8 px-6">
      <NuxtLink
        :to="partner.src"
        target="_blank"
        v-for="partner in partners"
        :key="partner.id"
        class="group flex items-center justify-center p-4 bg-custom-bg-secondary rounded-xl transition transform hover:-translate-y-1 hover:shadow-lg cursor-pointer"
      >
        <img
          :src="partner.logo"
          :alt="partner.name"
          class="h-12 w-auto object-contain grayscale group-hover:grayscale-0 transition"
        />
      </NuxtLink>
    </div>
  </section>
</template>
