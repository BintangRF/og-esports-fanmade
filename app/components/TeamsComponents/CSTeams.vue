<script setup>
import PlayerCard from "../PlayerCard.vue";

const players = [
  {
    nickname: "Chr1zN",
    name: "Christoffer Jung Storgaard",
    role: "IGL",
    image: "/teams/cs2/CHR1ZN.webp",
    country: "Denmark",
    yearsActive: 7,
    achievements: 3,
    socials: [
      { name: "twitter", url: "https://twitter.com/chr1zn" },
      { name: "youtube", url: "https://youtube.com/chr1zn" },
    ],
  },
  {
    nickname: "Spooke",
    name: "Olle Grundström",
    role: "Rifler",
    image: "/teams/cs2/SPOOKE.webp",
    country: "Sweden",
    yearsActive: 5,
    achievements: 2,
    socials: [
      { name: "twitter", url: "https://twitter.com/spooke" },
      { name: "instagram", url: "https://instagram.com/spooke" },
    ],
  },
  {
    nickname: "nicoodoz",
    name: "Nico Tamjidi",
    role: "AWPer",
    image: "/teams/cs2/NICOODOZ.webp",
    country: "Denmark",
    yearsActive: 4,
    achievements: 1,
    socials: [{ name: "twitter", url: "https://twitter.com/nicoodoz" }],
  },
  {
    nickname: "Vladyslava",
    name: "Vladyslava Zakhliebina",
    role: "CS2 Team Manager",
    image: "/teams/cs2/VLADYSLAVA.webp",
    country: "Ukraine",
    yearsActive: 6,
    achievements: 2,
    socials: [{ name: "instagram", url: "https://instagram.com/vladyslava" }],
  },
  {
    nickname: "Lambert",
    name: "Lambert Prigent",
    role: "Coach",
    image: "/teams/cs2/LAMBERT.webp",
    country: "France",
    yearsActive: 8,
    achievements: 4,
    socials: [
      { name: "twitter", url: "https://twitter.com/lambert" },
      { name: "youtube", url: "https://youtube.com/lambert" },
    ],
  },
  {
    nickname: "killazoo",
    name: "Adrien Legarda",
    role: "Assistant Coach",
    image: "/teams/cs2/KILLAZOO.webp",
    country: "France",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/killazoo" },
      { name: "youtube", url: "https://youtube.com/killazoo" },
    ],
  },
  {
    nickname: "adamb",
    name: "Adam Ångström",
    role: "Rifler",
    image: "/teams/cs2/ADAMB.webp",
    country: "Sweden",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/adamb" },
      { name: "youtube", url: "https://youtube.com/adamb" },
    ],
  },
  {
    nickname: "Arrozdoce",
    name: "Rafael Wing Ribeiro",
    role: "Rifler",
    image: "/teams/cs2/ARROZDOCE.webp",
    country: "Portugal",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/arrozdoce" },
      { name: "youtube", url: "https://youtube.com/arrozdoce" },
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
