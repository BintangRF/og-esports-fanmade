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

// Pagination setup
const currentPage = ref(1);
const perPage = 2;

const totalPages = computed(() => Math.ceil(newsList.length / perPage));

const paginatedNews = computed(() => {
  const start = (currentPage.value - 1) * perPage;
  return newsList.slice(start, start + perPage);
});

const goToPage = (page) => {
  if (page >= 1 && page <= totalPages.value) {
    currentPage.value = page;
    window.scrollTo({ top: 0, behavior: "smooth" });
  }
};
</script>

<template>
  <div class="py-16 space-y-3.5">
    <!-- Heading -->
    <div class="mx-auto text-center">
      <h1 class="text-3xl md:text-4xl font-bold text-custom-text-primary">
        OG Esports News
      </h1>
      <p class="text-custom-text-tertiary mt-3 text-base md:text-lg">
        Stay updated with the latest news and stories from all OG divisions.
      </p>
    </div>

    <!-- News Grid -->
    <div class="px-6 space-y-3.5 flex flex-col items-center">
      <NewsCard v-for="news in paginatedNews" :key="news.id" :news="news" />
    </div>

    <!-- Pagination -->
    <div class="flex justify-center space-x-2">
      <!-- Prev -->
      <button
        @click="goToPage(currentPage - 1)"
        :disabled="currentPage === 1"
        class="px-4 py-2 text-sm font-bold uppercase tracking-wide transition-all duration-200"
        :class="
          currentPage === 1
            ? 'bg-custom-bg-secondary text-custom-text-secondary cursor-not-allowed border-2 border-custom-accent-secondary'
            : 'bg-custom-bg-secondary text-custom-text-primary hover:bg-custom-accent-primary shadow-lg border-2 cursor-pointer'
        "
      >
        Prev
      </button>

      <!-- Numbered pages -->
      <button
        v-for="page in totalPages"
        :key="page"
        @click="goToPage(page)"
        class="px-4 py-2 text-sm font-bold uppercase tracking-wide transition-all duration-200"
        :class="
          page === currentPage
            ? 'bg-custom-accent-primary text-custom-text-primary border-2 border-custom-text-primary shadow-lg'
            : 'bg-transparent text-custom-text-primary border-custom-accent-secondary border-2 cursor-pointer'
        "
      >
        {{ page }}
      </button>

      <!-- Next -->
      <button
        @click="goToPage(currentPage + 1)"
        :disabled="currentPage === totalPages"
        class="px-4 py-2 text-sm font-bold uppercase tracking-wide transition-all duration-200"
        :class="
          currentPage === totalPages
            ? 'bg-custom-bg-secondary text-custom-text-secondary cursor-not-allowed border-2 border-custom-accent-secondary'
            : 'bg-custom-bg-secondary text-custom-text-primary hover:bg-custom-accent-primary shadow-lg border-2 cursor-pointer'
        "
      >
        Next
      </button>
    </div>
  </div>
</template>
