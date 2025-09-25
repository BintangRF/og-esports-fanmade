<script setup>
import CSTeams from "./CSTeams.vue";
import DotaTeams from "./DotaTeams.vue";
import EAFCTeams from "./EAFCTeams.vue";
import HokTeams from "./HokTeams.vue";
import MarvelTeams from "./MarvelTeams.vue";
import MlTeams from "./MlTeams.vue";

const tabs = [
  { name: "Dota 2" },
  { name: "Honor of Kings" },
  { name: "Mobile Legends" },
  { name: "CS2" },
  { name: "Marvel Rivals" },
  { name: "EAFC" },
];

const activeTab = ref("Dota 2");

const selectTab = (tab) => {
  activeTab.value = tab;
};
</script>

<template>
  <div class="py-16 space-y-3.5">
    <!-- Heading -->
    <div class="mx-auto text-center my-10 px-4">
      <h1 class="text-3xl md:text-4xl font-bold text-custom-text-primary">
        OG Esports Teams
      </h1>
      <p
        class="text-custom-text-tertiary mt-3 text-base md:text-lg max-w-2xl mx-auto"
      >
        Meet our rosters across multiple esports divisions.
      </p>
    </div>

    <!-- Tabs -->
    <div class="flex justify-center gap-3 flex-wrap">
      <button
        v-for="tab in tabs"
        :key="tab.name"
        @click="selectTab(tab.name)"
        class="flex items-center gap-2 px-5 py-2 font-bold transition-all uppercase text-custom-text-primary shadow-md"
        :class="
          activeTab === tab.name
            ? 'bg-custom-accent-primary border-2 border-custom-bg-primary ring-2 ring-custom-accent-primary '
            : 'bg-transparent border-2 border-custom-accent-secondary cursor-pointer'
        "
      >
        {{ tab.name }}
      </button>
    </div>

    <!-- Content -->
    <div
      class="max-w-7xl mx-auto px-6 mb-10 text-center text-custom-text-primary"
    >
      <div class="p-6 mt-8">
        <transition name="fade" mode="out-in">
          <!-- Dota 2 -->
          <div v-if="activeTab === 'Dota 2'" key="dota2">
            <h2 class="text-2xl font-bold text-custom-accent">OG Dota 2</h2>
            <p class="mt-4 leading-relaxed">
              OG is a professional Dota 2 team known for their multiple The
              International victories and innovative playstyle.
            </p>

            <DotaTeams />
          </div>

          <!-- Honor of Kings -->
          <div v-else-if="activeTab === 'Honor of Kings'" key="hok">
            <h2 class="text-2xl font-bold text-custom-accent">
              OG Honor of Kings
            </h2>
            <p class="mt-4 leading-relaxed">
              A formidable presence in the Honor of Kings scene, showcasing
              exceptional teamwork and strategy.
            </p>

            <HokTeams />
          </div>

          <!-- Mobile Legends -->
          <div v-else-if="activeTab === 'Mobile Legends'" key="ml">
            <h2 class="text-2xl font-bold text-custom-accent">
              OG Mobile Legends: Bang Bang
            </h2>
            <p class="mt-4 leading-relaxed">
              The newest division of OG, ready to dominate the MPL scene.
            </p>

            <MlTeams />
          </div>

          <!-- CS2 -->
          <div v-else-if="activeTab === 'CS2'" key="cs">
            <h2 class="text-2xl font-bold text-custom-accent">OG CS2</h2>
            <p class="mt-4 leading-relaxed">
              Known for their firepower and tactical brilliance.
            </p>

            <CSTeams />
          </div>

          <!-- Marvel Rivals -->
          <div v-else-if="activeTab === 'Marvel Rivals'" key="marvel">
            <h2 class="text-2xl font-bold text-custom-accent">
              OG Marvel Rivals
            </h2>
            <p class="mt-4 leading-relaxed">
              Explosive gameplay and bold strategies in the new competitive
              scene.
            </p>

            <MarvelTeams />
          </div>

          <!-- EAFC -->
          <div v-else-if="activeTab === 'EAFC'" key="eafc">
            <h2 class="text-2xl font-bold text-custom-accent">OG EAFC</h2>
            <p class="mt-4 text-custom-text-tertiary leading-relaxed">
              Representing the future of digital football on the global stage.
            </p>

            <EAFCTeams />
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
