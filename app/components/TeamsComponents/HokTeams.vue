<script setup>
import PlayerCard from "../PlayerCard.vue";

const players = [
  {
    nickname: "keke",
    name: "Daniele Ke",
    role: "Clash",
    image: "/teams/hok/KEKE.webp",
    country: "China",
    yearsActive: 7,
    achievements: 3,
    socials: [
      { name: "twitter", url: "https://twitter.com/keke" },
      { name: "youtube", url: "https://youtube.com/keke" },
    ],
  },
  {
    nickname: "DaoDao",
    name: "Jiale Qian",
    role: "Jungle",
    image: "/teams/hok/DAODAO.webp",
    country: "China",
    yearsActive: 5,
    achievements: 2,
    socials: [
      { name: "twitter", url: "https://twitter.com/daodao" },
      { name: "instagram", url: "https://instagram.com/daodao" },
    ],
  },
  {
    nickname: "Wen",
    name: "Ren Hao Guan",
    role: "Mid",
    image: "/teams/hok/WEN.webp",
    country: "China",
    yearsActive: 4,
    achievements: 1,
    socials: [{ name: "twitter", url: "https://twitter.com/wen" }],
  },
  {
    nickname: "an",
    name: "Junan Lin",
    role: "Farm Lane",
    image: "/teams/hok/AN.webp",
    country: "China",
    yearsActive: 6,
    achievements: 2,
    socials: [{ name: "instagram", url: "https://instagram.com/an" }],
  },
  {
    nickname: "muchen",
    name: "Angelo Zheng",
    role: "Roamer",
    image: "/teams/hok/MUCHEN.webp",
    country: "China",
    yearsActive: 8,
    achievements: 4,
    socials: [
      { name: "twitter", url: "https://twitter.com/muchen" },
      { name: "youtube", url: "https://youtube.com/muchen" },
    ],
  },
  {
    nickname: "Sya",
    name: "Sabrina Starke",
    role: "Manager",
    image: "/placeholder.webp",
    country: "Germany",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/sya" },
      { name: "youtube", url: "https://youtube.com/sya" },
    ],
  },
  {
    nickname: "Andy",
    name: "Jie Zhang",
    role: "Coach",
    image: "/placeholder.webp",
    country: "China",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/andy" },
      { name: "youtube", url: "https://youtube.com/andy" },
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
