<template>
  <nav class="Tabs">
    <header
      class="w-full flex justify-center capitalize cursor-pointer text-center"
    >

    <!-- <Badge
    @click="PokemonStore.AddFavouritePokemon"
    v-if="!PokemonStore.pokemonEmpty"
    class=" mr-1 mb-1 [&_img]:hover:scale-105 z-100	">
    <img v-if="!PokemonStore.isPokemonFavourite()" src="/heart.svg" class=" w-5 transition-transform" />
    <img v-else src="/bug.svg" class=" w-5 transition-transform" />

    </Badge> -->
    <Add />

      <Badge
        v-for="(label, tab) in tabs"
        @click="tabSelected = tab.toString()"
        :class="{
          'font-semibold bg-slate-100 dark:bg-slate-700': tab === tabSelected,
        }"
        class="py-2 px-6 whitespace-nowrap text-black dark:text-white"
        >{{ label }}</Badge
      >
    </header>

    <div class="mt-3"></div>

    <template v-for="(_, tab) in tabs">
      <slot v-if="tab === tabSelected" :name="tab"></slot>
    </template>
  </nav>
</template>

<script setup lang="ts">
const PokemonStore = usePokemonStore();

interface Tabs {
  [index: string]: string;
}
interface Props {
  tabs: Tabs;
}

const props = defineProps<Props>();

const tabSelected = ref(Object.keys(props.tabs)[0]);
</script>
