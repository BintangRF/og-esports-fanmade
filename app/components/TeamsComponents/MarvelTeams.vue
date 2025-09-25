<script setup>
import PlayerCard from "../PlayerCard.vue";

const players = [
  {
    nickname: "AbooHuu",
    name: "Abdellatif Alzaben",
    role: "Vanguard",
    image: "/placeholder.webp",
    country: "Saudi Arabia",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/aboohuu" },
      { name: "youtube", url: "https://youtube.com/aboohuu" },
    ],
  },
  {
    nickname: "Gainer",
    name: "Devan Cevik",
    role: "Vanguard",
    image: "/placeholder.webp",
    country: "Germany",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/gainer" },
      { name: "youtube", url: "https://youtube.com/gainer" },
    ],
  },
  {
    nickname: "FrostMountain",
    name: "Ahmad Graoui",
    role: "Duelist",
    image: "/placeholder.webp",
    country: "United Kingdom",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/frostmountain" },
      { name: "youtube", url: "https://youtube.com/frostmountain" },
    ],
  },
  {
    nickname: "Kq43",
    name: "Khalifa Al Qaizi",
    role: "Duelist",
    image: "/placeholder.webp",
    country: "UAE",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/kq43" },
      { name: "youtube", url: "https://youtube.com/kq43" },
    ],
  },
  {
    nickname: "Lapsisotilas",
    name: "Veeti Jäykkä",
    role: "Sub Strategist",
    image: "/placeholder.webp",
    country: "Finland",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/lapsisotilas" },
      { name: "youtube", url: "https://youtube.com/lapsisotilas" },
    ],
  },
  {
    nickname: "Namme",
    name: "Andrei Caran",
    role: "Strategist",
    image: "/placeholder.webp",
    country: "Romania",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/namme" },
      { name: "youtube", url: "https://youtube.com/namme" },
    ],
  },
  {
    nickname: "Hachikobtw",
    name: "Nicholas Bennett",
    role: "Vanguard",
    image: "/placeholder.webp",
    country: "Denmark",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/hachikobtw" },
      { name: "youtube", url: "https://youtube.com/hachikobtw" },
    ],
  },
  {
    nickname: "Statiic",
    name: "Nicholas Bennett",
    role: "Strategist",
    image: "/placeholder.webp",
    country: "Ukraine",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/biomachina" },
      { name: "youtube", url: "https://youtube.com/biomachina" },
    ],
  },
  {
    nickname: "Statiic",
    name: "Trent Lucas",
    role: "Coach",
    image: "/placeholder.webp",
    country: "USA",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/statiic" },
      { name: "youtube", url: "https://youtube.com/statiic" },
    ],
  },
  {
    nickname: "Schon",
    name: "Schon Hale",
    role: "Manager & Analyst",
    image: "/placeholder.webp",
    country: "USA",
    yearsActive: 10,
    achievements: 6,
    socials: [
      { name: "twitter", url: "https://twitter.com/schon" },
      { name: "youtube", url: "https://youtube.com/schon" },
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
