<template>
  <article
    :class="{
      'animate-pulse disabled': PokemonStore.pokemonEmpty,
    }"
    class="Card w-full rounded-3xl"
  >
    <!-- header -->
    <header
      :style="{ background: PokemonStore.getColor }"
      :class="{ 'bg-slate-300 dark:bg-slate-700': PokemonStore.pokemonEmpty }"
      class="flex flex-col-reverse items-center md:flex-row md:justify-between text-center md:text-left text-white relative rounded-t-3xl p-8 pb-10"
    >
      <span
        v-text="PokemonStore.getCode"
        class="absolute text-7xl font-medium top-10 md:left-4 md:top-4 opacity-25"
      ></span>

      <div class="parallax relative z-10">
        <div data-depth=".3">
          <h4
            v-text="PokemonStore.getName"
            class="font-semibold w-full md:w-2/4 text-4xl tracking-wide capitalize mb-4"
          ></h4>
          <Badge
            v-for="text in PokemonStore.getTypes"
            v-text="text"
            class="types mr-1 mb-1"
          ></Badge>
        </div>
      </div>

      <div class="parallax">
        <img
          data-depth="1"
          :src="PokemonStore.getImage"
          class="avatar h-40 -mt-32 md:-mt-20 drop-shadow-xl"
        />
      </div>
    </header>

    <!-- info -->
    <aside
      class="info w-full relative rounded-3xl overflow-hidden p-4 pt-8 -mt-6 z-10 bg-white dark:bg-slate-800"
    >
      <Tabs
        :tabs="{
          about: 'About',
          stats: 'Base States',
        }"
        class="mb-5"
      >
      
        <template #about>
          <!-- description -->
          <p v-text="PokemonStore.getAbout" class="text-sm mb-2 p-3"></p>

          <!-- more -->
          <div
            class="flex rounded-lg [&_>div]:p-2 [&_>div]:px-4 [&_>div]:flex-1 [&_>div>p]:text-slate-400 [&_>div>span]:font-medium text-sm px-2 py-1 bg-slate-50 dark:bg-slate-700"
          >
            <div>
              <p>Code</p>
              <span v-text="PokemonStore.getCode"></span>
            </div>
            <div>
              <p>Height</p>
              <span v-text="PokemonStore.getHeight"></span>
            </div>
            <div>
              <p>Weight</p>
              <span v-text="PokemonStore.getWeight"></span>
            </div>
          </div>

          <!-- abilities -->
          <h4 class="mt-5 font-medium p-2 font-xs">Abilities</h4>

          <div class="flex flex-wrap justify-center md:justify-start">
            <Badge
              v-for="ability in PokemonStore.getAbilities"
              v-text="ability"
              class="m-1 text-black dark:text-white bg-slate-50 dark:bg-slate-700"
            />
          </div>

          <!-- Weaknesses -->
          <h4 class="mt-2 font-medium p-2 font-xs">Weaknesses</h4>

          <div class="flex flex-wrap justify-center md:justify-start">
            <Badge
              v-for="weakness in PokemonStore.getWeaknesses"
              :style="{
                background: PokemonStore.types[weakness],
              }"
              class="m-1 text-white"
            >
              <img :src="`/${weakness}.svg`" class="mr-2 w-3" />
              <span v-text="weakness"></span>
            </Badge>
          </div>
        </template>

        <!-- stats -->
        <template #stats>
          <div class="mt-5"></div>
          <Stats
            v-for="(percent, label) in PokemonStore.getStats"
            :color="PokemonStore.getColor"
            :percent="percent"
            :label="label.toString()"
          />
        </template>
      </Tabs>
    </aside>
  </article>
</template>

<script setup lang="ts">
const PokemonStore = usePokemonStore();
</script>

<style scoped>
.Card {
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.05);
}
.info {
  min-height: 300px;
}
.types {
  background: rgba(255, 255, 255, 0.2);
}
.avatar {
  min-width: 160px;
}
</style>
