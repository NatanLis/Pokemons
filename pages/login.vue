<template>
  <div :class="{ dark: dark }">
    <section
      class="App min-h-screen p-6 pb-0 lg:px-20 max-w-full overflow-x-hidden dark:text-white dark:bg-slate-900"
    >
      <header class="relative w-full flex justify-between items-center">
        <img src="/pokemon.svg" class="w-32" />
        <DarkMode @change="changeDarkMode" class="z-10"/>
      </header>
      <div class="flex items-center justify-center text-not-that-higher mt-6 sm:mt-0">
        <div class="relative isolate lg:px-8">
          <Polygon />

          <div class="mx-auto max-w-3xl py-16 sm:py-24 lg:py-32">
            <div class="hidden sm:mb-8 sm:flex sm:justify-center">
            </div>
            <div class="text-center">
              <!-- <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-7xl  dark:text-white">Log in, Trainer</h1> -->
              <!-- <div  class="my-2 relative overflow-hidden">
                <img src="/stars.svg" alt="" class="mx-auto">
                <img v-if="dark" src="/img-pokeball-blue.png" alt="" class="mx-auto">
                <img  v-if="!dark" src="/img-pokeball-red.png" alt="" class="mx-auto">
              </div> -->
              <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-7xl  dark:text-white">Log in, Trainer</h1>

              <p class="mt-6 text-higher text-lg leading-8 text-gray-600 dark:text-white dark:opacity-75">
                Hop in and start your journey to become the ultimate Pokémon trainer.
              </p>

              <form @submit.prevent="handleSubmit" class="mt-8 space-y-6">
                <div class="rounded-md shadow-sm space-y-4 text-left">
                  <div>
                    <label for="email"  class="block text-sm font-medium text-gray-700 dark:text-gray-300">Email address</label>
                    <input id="email" v-model="email" name="email" type="email" required
                      class="mt-1 relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm dark:bg-slate-800 dark:border-gray-700 dark:text-white"
                      placeholder="Email address">
                  </div>
                  <div>
                    <label for="password" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Password</label>
                    <input id="password" v-model="password" name="password" type="password" required
                      class="mt-1 relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm dark:bg-slate-800 dark:border-gray-700 dark:text-white"
                      placeholder="Password">
                  </div>
                </div>

                <h2 v-if="error" class="text-2xl text-red-600 dark:text-indigo-500 dark:opacity-75">
                  Something went wrong. Try again trainer!
                </h2>

                <div class="mt-6 flex justify-center">
                  <button type="submit"
                    class="added-transition rounded-md bg-red-600 dark:bg-indigo-600 px-4 py-2 text-sm font-semibold text-white shadow-sm hover:bg-red-700 dark:hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                    Log in
                  </button>
                </div>
              </form>

              <p class=" text-sm text-gray-600 dark:text-gray-400">
                Do not have an account?
                <NuxtLink to="/signup" class="font-medium text-red-600 dark:text-indigo-600 hover:text-red-700 dark:hover:text-indigo-700">
                  Create one
                </NuxtLink>
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import { useRoute, Router } from 'vue-router';
// import { useCookie } from 'vue-cookie-next';
import { ref } from 'vue';

const router = useRoute();

const dark = useCookie<boolean>("dark");

console.log(dark);


const email = ref('');
const password = ref('');
const password2 = ref('');
const error = ref(false);

function changeDarkMode(isDark: boolean): void {
  dark.value = isDark;
}

function handleSubmit() {
  console.log('Form submitted - start');
  console.log(email.value, password.value, password2.value);
  error.value = false;

  if (password.value !== password2.value) {
    // alert('Passwords do not match');
    error.value = true;
    return;
  }

  // router.push({ path: "/pokemons" });
  router.push("/pokemons");
  console.log('Form submitted- end');
  }
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
@keyframes float {
	0% {
		transform: translateY(0px);
	}
	50% {
		transform: translateY(-20px);
	}
	100% {
		transform: translateY(0px);
	}
}


@keyframes circle {
	0% {
		transform: rotate(0deg);
	}
	10% {
		transform: rotate(36deg);
	}
	20% {
		transform: rotate(72deg);
	}
	30% {
		transform: rotate(108deg);
	}
	40% {
		transform: rotate(144deg);
	}
	50% {
		transform: rotate(180deg);
	}
	60% {
		transform: rotate(216deg);
	}
	70% {
		transform: rotate(252deg);
	}
	80% {
		transform: rotate(288deg);
	}
	90% {
		transform: rotate(324deg);
	}
	100% {
		transform: rotate(360deg);
	}
}

.text-higher{
  position: relative;
  top: -145px;
}
.text-not-that-higher{
  position: relative;
  top: -80px;
}

.added-transition {
  transition: 0.5s !important;
}
.added-transition:hover {
  top: -4px;
}

.rickVideo{
    aspect-ratio: 16 / 9 !important;
    width: 100% !important;
}
</style>
