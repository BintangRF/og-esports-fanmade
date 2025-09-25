<template>
  <div class="py-16 space-y-24 text-custom-text-primary">
    <!-- Heading -->
    <div class="mx-auto text-center max-w-3xl px-6">
      <h1 class="text-4xl md:text-5xl font-bold text-custom-text-primary mb-6">
        About OG Esports
      </h1>
      <p class="text-custom-text-tertiary text-lg leading-relaxed">
        Founded in 2015, OG Esports has become a legendary name in the world of
        competitive gaming. From conquering
        <span class="font-semibold text-custom-text-primary"
          >The International</span
        >
        twice to expanding into multiple gaming divisions, OG continues to
        inspire millions of fans with passion, resilience, and unmatched
        teamwork.
      </p>
    </div>

    <!-- Story with Image -->
    <div
      class="px-6 grid grid-cols-1 lg:grid-cols-2 gap-16 items-center max-w-7xl mx-auto"
    >
      <div class="order-2 lg:order-1">
        <h3 class="text-2xl font-bold text-custom-text-primary mb-6">
          Our Journey
        </h3>
        <p class="text-custom-text-tertiary leading-relaxed mb-6">
          OG was founded by a group of passionate players who believed in
          breaking limits and rewriting esports history. In 2018 and 2019, OG
          shocked the world by becoming the first team to win
          <span class="font-semibold text-custom-text-primary"
            >back-to-back The International titles</span
          >.
        </p>
        <p class="text-custom-text-tertiary leading-relaxed">
          Today, OG has expanded beyond Dota 2 into multiple games, while
          continuing to push the boundaries of what an esports organization can
          achieve.
        </p>
      </div>
      <div class="order-1 lg:order-2">
        <div
          class="relative overflow-hidden rounded-2xl shadow-xl border border-custom-accent-secondary"
        >
          <img
            src="/ti-win.webp"
            alt="OG Winning Moment"
            class="w-full aspect-video object-cover transition-transform duration-500 hover:scale-105"
          />
        </div>
      </div>
    </div>

    <!-- Vision & Mission -->
    <div class="px-6 grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
      <div
        class="p-8 rounded-xl shadow-lg bg-custom-bg-secondary border border-custom-accent-secondary transition-all duration-300 hover:border-custom-accent-secondary/30 hover:bg-custom-bg-secondary/70"
      >
        <h3 class="text-xl font-semibold text-custom-text-primary mb-4">
          Our Vision
        </h3>
        <p class="text-custom-text-tertiary leading-relaxed">
          To be a global symbol of excellence in esports, inspiring future
          generations to dream big and pursue greatness both inside and outside
          the game.
        </p>
      </div>
      <div
        class="p-8 rounded-xl shadow-lg bg-custom-bg-secondary border border-custom-accent-secondary transition-all duration-300 hover:border-custom-accent-secondary/30 hover:bg-custom-bg-secondary/70"
      >
        <h3 class="text-xl font-semibold text-custom-text-primary mb-4">
          Our Mission
        </h3>
        <p class="text-custom-text-tertiary leading-relaxed">
          Empower players, engage fans, and expand esports into a sustainable,
          inclusive, and innovative industry that unites communities worldwide.
        </p>
      </div>
    </div>

    <!-- Core Values -->
    <div class="px-6 max-w-6xl mx-auto">
      <h3 class="text-2xl font-bold text-center mb-12">
        Core Values We Believe In
      </h3>
      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 text-center"
      >
        <div
          class="p-6 rounded-xl border border-custom-accent-secondary transition-all duration-300 hover:border-custom-accent-secondary/50 hover:bg-custom-bg-secondary/40"
        >
          <h4 class="font-semibold mb-3 text-lg">Teamwork</h4>
          <p class="text-sm text-custom-text-tertiary">
            Stronger together, always united.
          </p>
        </div>
        <div
          class="p-6 rounded-xl border border-custom-accent-secondary transition-all duration-300 hover:border-custom-accent-secondary/50 hover:bg-custom-bg-secondary/40"
        >
          <h4 class="font-semibold mb-3 text-lg">Passion</h4>
          <p class="text-sm text-custom-text-tertiary">
            Fueled by love for the game.
          </p>
        </div>
        <div
          class="p-6 rounded-xl border border-custom-accent-secondary transition-all duration-300 hover:border-custom-accent-secondary/50 hover:bg-custom-bg-secondary/40"
        >
          <h4 class="font-semibold mb-3 text-lg">Innovation</h4>
          <p class="text-sm text-custom-text-tertiary">
            Pioneering new strategies & ideas.
          </p>
        </div>
        <div
          class="p-6 rounded-xl border border-custom-accent-secondary transition-all duration-300 hover:border-custom-accent-secondary/50 hover:bg-custom-bg-secondary/40"
        >
          <h4 class="font-semibold mb-3 text-lg">Resilience</h4>
          <p class="text-sm text-custom-text-tertiary">
            Never giving up, no matter what.
          </p>
        </div>
      </div>
    </div>

    <!-- Divisions Section -->
    <div class="px-6 max-w-7xl mx-auto">
      <h3 class="text-2xl font-bold text-center mb-12">
        Our Esports Divisions
      </h3>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          class="rounded-xl overflow-hidden shadow-lg border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:shadow-xl"
        >
          <div class="relative overflow-hidden">
            <img
              src="/dota.webp"
              alt="Dota 2"
              class="w-full aspect-video object-cover transition-transform duration-500 hover:scale-105"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-custom-accent-secondary/50 to-transparent"
            ></div>
          </div>
          <div class="p-6">
            <h4 class="text-xl font-semibold text-custom-text-primary">
              Dota 2
            </h4>
            <p class="text-sm text-custom-text-tertiary mt-2">
              The legendary squad that made history with back-to-back TI wins.
            </p>
          </div>
        </div>
        <div
          class="rounded-xl overflow-hidden shadow-lg border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:shadow-xl"
        >
          <div class="relative overflow-hidden">
            <img
              src="/cs.webp"
              alt="CS:GO"
              class="w-full aspect-video object-cover transition-transform duration-500 hover:scale-105"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-custom-accent-secondary/50 to-transparent"
            ></div>
          </div>
          <div class="p-6">
            <h4 class="text-xl font-semibold text-custom-text-primary">
              CS:GO
            </h4>
            <p class="text-sm text-custom-text-tertiary mt-2">
              OG entered the FPS scene with a talented roster competing at the
              highest level.
            </p>
          </div>
        </div>
        <div
          class="rounded-xl overflow-hidden shadow-lg border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:shadow-xl"
        >
          <div class="relative overflow-hidden">
            <img
              src="/ml.webp"
              alt="Mobile Legends"
              class="w-full aspect-video object-cover transition-transform duration-500 hover:scale-105"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-custom-accent-secondary/50 to-transparent"
            ></div>
          </div>
          <div class="p-6">
            <h4 class="text-xl font-semibold text-custom-text-primary">
              Mobile Legends
            </h4>
            <p class="text-sm text-custom-text-tertiary mt-2">
              Expanding into SEA's most popular MOBA to inspire the next
              generation of gamers.
            </p>
          </div>
        </div>
        <div
          class="rounded-xl overflow-hidden shadow-lg border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:shadow-xl"
        >
          <div class="relative overflow-hidden">
            <img
              src="/marvel.webp"
              alt="Marvel Rivals"
              class="w-full aspect-video object-cover transition-transform duration-500 hover:scale-105"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-custom-accent-secondary/50 to-transparent"
            ></div>
          </div>
          <div class="p-6">
            <h4 class="text-xl font-semibold text-custom-text-primary">
              Marvel Rivals
            </h4>
            <p class="text-sm text-custom-text-tertiary mt-2">
              A fresh challenge where OG showcases adaptability in new arenas.
            </p>
          </div>
        </div>
        <div
          class="rounded-xl overflow-hidden shadow-lg border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:shadow-xl"
        >
          <div class="relative overflow-hidden">
            <img
              src="/eafc.webp"
              alt="EAFC"
              class="w-full aspect-video object-cover transition-transform duration-500 hover:scale-105"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-custom-accent-secondary/50 to-transparent"
            ></div>
          </div>
          <div class="p-6">
            <h4 class="text-xl font-semibold text-custom-text-primary">EAFC</h4>
            <p class="text-sm text-custom-text-tertiary mt-2">
              Bringing OG spirit into the world of football esports and global
              competition.
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Achievements -->
    <div class="px-6 max-w-4xl mx-auto">
      <h3 class="text-2xl font-bold text-center mb-12">
        Milestones & Achievements
      </h3>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div
          class="p-8 rounded-xl text-center border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:bg-custom-bg-secondary/60"
        >
          <p class="text-5xl font-bold mb-3 text-custom-text-primary">2x</p>
          <p class="text-custom-text-tertiary">The International Champion</p>
        </div>
        <div
          class="p-8 rounded-xl text-center border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:bg-custom-bg-secondary/60"
        >
          <p class="text-5xl font-bold mb-3 text-custom-text-primary">5+</p>
          <p class="text-custom-text-tertiary">Major Tournament Wins</p>
        </div>
        <div
          class="p-8 rounded-xl text-center border border-custom-accent-secondary bg-custom-bg-secondary/40 transition-all duration-300 hover:border-custom-accent-secondary/30 hover:bg-custom-bg-secondary/60"
        >
          <p class="text-5xl font-bold mb-3 text-custom-text-primary">10M+</p>
          <p class="text-custom-text-tertiary">Global Fans & Followers</p>
        </div>
      </div>
    </div>
  </div>
</template>
