<script setup>
import PlayerCard from "../PlayerCard.vue";

const players = [
  {
    nickname: "Kramm",
    name: "Mark Genzon Rusiana",
    role: "EXP Laner",
    image: "/teams/mlbb/KRAMM.webp",
    country: "Philippines",
    yearsActive: 7,
    achievements: 3,
    socials: [
      { name: "twitter", url: "https://twitter.com/kramm" },
      { name: "youtube", url: "https://youtube.com/kramm" },
    ],
  },
  {
    nickname: "Gojes",
    name: "Ilman Zareef",
    role: "EXP Laner",
    image: "/teams/mlbb/GOJES.webp",
    country: "Malaysia",
    yearsActive: 5,
    achievements: 2,
    socials: [
      { name: "twitter", url: "https://twitter.com/gojes" },
      { name: "instagram", url: "https://instagram.com/gojes" },
    ],
  },
  {
    nickname: "Sekys",
    name: "Muhammad Haqqullah",
    role: "Jungler",
    image: "/teams/mlbb/SEKYS.webp",
    country: "Malaysia",
    yearsActive: 4,
    achievements: 1,
    socials: [{ name: "twitter", url: "https://twitter.com/sekys" }],
  },
  {
    nickname: "Stormie",
    name: "Hazziq Danish",
    role: "Mid Laner",
    image: "/teams/mlbb/STORMIE.webp",
    country: "Malaysia",
    yearsActive: 6,
    achievements: 2,
    socials: [{ name: "instagram", url: "https://instagram.com/stormie" }],
  },
  {
    nickname: "Innocent",
    name: "John Vincent Banal",
    role: "Gold Laner",
    image: "/teams/mlbb/INNOCENT.webp",
    country: "Philippines",
    yearsActive: 8,
    achievements: 4,
    socials: [
      { name: "twitter", url: "https://twitter.com/innocent" },
      { name: "youtube", url: "https://youtube.com/innocent" },
    ],
  },
  {
    nickname: "Yums",
    name: "Muhammad Qayyum Ariffin",
    role: "Roamer",
    image: "/teams/mlbb/YUMS.webp",
    country: "Malaysia",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/yums" },
      { name: "youtube", url: "https://youtube.com/yums" },
    ],
  },
  {
    nickname: "Arcadia",
    name: "Michael Angelo Bocado",
    role: "Coach",
    image: "/teams/mlbb/ARCADIA.webp",
    country: "Philippines",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/arcadia" },
      { name: "youtube", url: "https://youtube.com/arcadia" },
    ],
  },
  {
    nickname: "OzoraVeki",
    name: "Poon Kok Sing",
    role: "Assistant Coach",
    image: "/teams/mlbb/OZORAVEKI.webp",
    country: "Malaysia",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/ozoraveki" },
      { name: "youtube", url: "https://youtube.com/ozoraveki" },
    ],
  },
  {
    nickname: "Amir",
    name: "Amir Syafiq",
    role: "TEAM MANAGER",
    image: "/placeholder.webp",
    country: "Malaysia",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/amir" },
      { name: "youtube", url: "https://youtube.com/amir" },
    ],
  },
];
</script>

<template>
  <div class="mt-8 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
    <PlayerCard
      v-for="player in players"
      :key="player.nickname"
      :nickname="player.nickname"
      :name="player.name"
      :role="player.role"
      :image="player.image"
      :country="player.country"
      :years-active="player.yearsActive"
      :achievements="player.achievements"
      :socials="player.socials"
    />
  </div>
</template>
