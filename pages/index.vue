<template>
  <div :class="{ dark: dark }">
    <section
      class="App min-h-screen p-6 pb-0 lg:px-20 max-w-full overflow-x-hidden dark:text-white dark:bg-slate-900"
    >
      <!-- header -->
      <header class="relative w-full flex justify-between items-center">

        <img src="/pokemon.svg" class="w-32" />

        <DarkMode @change="changeDarkMode" />
      </header>
      creating an account or log in

      <NuxtLink to="/pokemons">
        <p>pokemons website</p>
      </NuxtLink>
    </section>
  </div>
</template>

<script setup lang="ts">

// data
// const PokemonStore = usePokemonStore();
const dark = useCookie<boolean>("dark");

// methods
function changeDarkMode(isDark: boolean): void {
  dark.value = isDark;
}
// // onMounted
// onMounted( () => {
//   PokemonStore.get();
//   PokemonStore.getAll();
// });
</script>

<style>
body * {
  font-family: "Poppins", sans-serif;
}

.disabled {
  cursor: no-drop;
}

.disabled * {
  user-select: none;
  pointer-events: none !important;
}

.footer {
  /* background: rgb(55, 156, 250); */
}
</style>
