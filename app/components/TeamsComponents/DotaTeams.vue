<script setup>
import PlayerCard from "../PlayerCard.vue";

const players = [
  {
    nickname: "Daze",
    name: "Tamir Tokpanov",
    role: "Soft Support",
    image: "/teams/dota/DAZE.webp",
    country: "Kazakhstan",
    yearsActive: 7,
    achievements: 3,
    socials: [
      { name: "twitter", url: "https://twitter.com/daze" },
      { name: "youtube", url: "https://youtube.com/daze" },
    ],
  },
  {
    nickname: "Shad",
    name: "Indji Lub",
    role: "Carry",
    image: "/teams/dota/SHAD.webp",
    country: "Netherlands",
    yearsActive: 5,
    achievements: 2,
    socials: [
      { name: "twitter", url: "https://twitter.com/shad" },
      { name: "instagram", url: "https://instagram.com/shad" },
    ],
  },
  {
    nickname: "Stormstormer",
    name: "Daniel Schoetzau",
    role: "Midlaner",
    image: "/teams/dota/STORMSTORMER.webp",
    country: "Germany",
    yearsActive: 4,
    achievements: 1,
    socials: [{ name: "twitter", url: "https://twitter.com/stormstormer" }],
  },
  {
    nickname: "MikSa`",
    name: "Mihajlo Jovanovic",
    role: "Offlane",
    image: "/teams/dota/MIKSA.webp",
    country: "Serbia",
    yearsActive: 6,
    achievements: 2,
    socials: [{ name: "instagram", url: "https://instagram.com/miksa" }],
  },
  {
    nickname: "Kidaro",
    name: "Ivan Bondarev",
    role: "Hard Support",
    image: "/teams/dota/KIDARO.webp",
    country: "Ukraine",
    yearsActive: 8,
    achievements: 4,
    socials: [
      { name: "twitter", url: "https://twitter.com/kidaro" },
      { name: "youtube", url: "https://youtube.com/kidaro" },
    ],
  },
  {
    nickname: "Notail",
    name: "Johan Sundstein",
    role: "Coach",
    image: "/teams/dota/NOTAIL.webp",
    country: "Faroe Islands",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/notail" },
      { name: "youtube", url: "https://youtube.com/notail" },
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
