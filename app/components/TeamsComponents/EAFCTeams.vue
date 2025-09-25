<script setup>
import PlayerCard from "../PlayerCard.vue";

const players = [
  {
    nickname: "Buzzinho",
    name: "Khevind Awat-Ranai",
    role: "Player",
    image: "/teams/eafc/BUZZINHO.webp",
    country: "Malaysia",
    yearsActive: 7,
    achievements: 3,
    socials: [
      { name: "twitter", url: "https://twitter.com/buzzinho" },
      { name: "youtube", url: "https://youtube.com/buzzinho" },
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
