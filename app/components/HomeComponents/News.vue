<script setup>
import NewsCard from "~/components/NewsCard.vue";

const newsList = [
  {
    id: 1,
    title: "OG Esports Officially Launched Their New Jersey",
    image: "/news/news-jersey.webp",
    category: "Dota 2",
    date: "2 hours ago • 4 min read",
    excerpt:
      "We proudly unveiled our newest jersey during a grand ceremony. The sleek design blends modern aesthetics and classic elements, making it a true eye-catcher.",
  },
  {
    id: 2,
    title: "OG Dominates the Blast Premier",
    image: "/news/news-cs.webp",
    category: "CS",
    date: "1 day ago • 6 min read",
    excerpt:
      "OG CS squad showed an outstanding performance, securing a spot in the Blast Premier playoffs.",
  },
  {
    id: 3,
    title: "Marvel Rivals Division Shows Strong Debut",
    image: "/news/news-marvel.webp",
    category: "Marvel Rivals",
    date: "3 days ago • 5 min read",
    excerpt:
      "OG's Marvel Rivals team made an impressive debut, turning heads with bold plays and smart strategies.",
  },
  {
    id: 4,
    title: "OG EAFC Team Qualifies for Global Series",
    image: "/news/news-eafc.webp",
    category: "EAFC",
    date: "1 week ago • 4 min read",
    excerpt:
      "OG EAFC players have officially qualified for the EA Sports FC Global Series, marking a huge step forward.",
  },
  {
    id: 5,
    title: "Mobile Legends Division Enters MPL",
    image: "/news/news-ml.webp",
    category: "Mobile Legends",
    date: "2 weeks ago • 3 min read",
    excerpt:
      "OG confirms their entry into the MPL scene, aiming to bring their championship spirit into Mobile Legends.",
  },
];
</script>

<template>
  <div class="py-16 space-y-3.5">
    <!-- Heading -->
    <h2 class="text-2xl text-center font-bold text-custom-text-primary">
      Latest News
    </h2>

    <!-- News Card -->
    <div class="px-6 space-y-3.5 flex flex-col items-center">
      <NewsCard v-for="news in newsList" :key="news.id" :news="news" />
    </div>

    <!-- View All Button -->
    <div class="flex justify-center">
      <NuxtLink
        to="/news"
        class="px-6 py-2 border-2 border-custom-accent-primary text-custom-accent-primary hover:bg-custom-accent-primary hover:text-custom-text-primary transition font-semibold uppercase tracking-wide"
      >
        View All News
      </NuxtLink>
    </div>
  </div>
</template>
