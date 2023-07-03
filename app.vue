<template>
  <div>
    <!-- Markup shared across all pages, ex: NavBar -->
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">

// data
const PokemonStore = usePokemonStore();

// console.log(PokemonStore.pokemon.name)

//  if (PokemonStore) {
//   PokemonStore.getAll();
//   PokemonStore.get();
//  }
// onMounted
// onMounted(async () => {
//   await PokemonStore.getAll();
//   await PokemonStore.get();
// });
</script>
