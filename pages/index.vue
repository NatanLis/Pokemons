<template>
  <div :class="{ dark: dark }">
    <section
      class="App min-h-screen p-6 pb-0 lg:px-20 max-w-full overflow-x-hidden dark:text-white dark:bg-slate-900"
    >
      <!-- header -->
      <header class="relative w-full flex justify-between items-center">
        <img src="/pokemon.svg" class="w-32" />
        <DarkMode @change="changeDarkMode" class="z-10"/>
      </header>
      <div class="flex items-center justify-center text-not-that-higher mt-6 sm:mt-0">
        <div class="relative isolate lg:px-8">
          <div  style="animation: circle 55s ease-in-out infinite;" class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-100" aria-hidden="true">
            <div v-if="!dark"  class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
            <div v-if="dark" class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#fff] to-[#4F46E5] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
          </div>
            <div  style="animation: circle 95s ease-in-out infinite;" class="absolute inset-x-0 -top-40 right-0 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-100" aria-hidden="true">
              <div v-if="!dark"  class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#f00] to-[#f00] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(50% 0%, 61% 35%, 100% 0, 65% 45%, 100% 100%, 49% 53%, 0 100%, 33% 46%, 0 0, 39% 35%);" />
              <div v-if="dark" class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#fff] to-[#4F46E5] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(50% 0%, 61% 35%, 100% 0, 65% 45%, 100% 100%, 49% 53%, 0 100%, 33% 46%, 0 0, 39% 35%);)" />
            </div>
          <div class="mx-auto max-w-2xl py-16 sm:py-24 lg:py-32">
            <div class="hidden sm:mb-8 sm:flex sm:justify-center">
              <div  class="relative rounded-full px-3 py-1 text-sm leading-6 text-gray-600 ring-1 ring-gray-900/10 dark:ring-white-900 hover:ring-gray-900/20">
                We are announcing the next round of financing our studies <a href="#" target="" class="font-semibold text-red-600 dark:text-indigo-600"><span class="absolute inset-0" aria-hidden="true" />Pleas help <span aria-hidden="true">&rarr;</span></a>
              </div>
            </div>
            <div class="text-center">
              <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-7xl  dark:text-white">Can you catch them all?</h1>
              <div  class="my-2 relative overflow-hidden" style="animation: float 6s ease-in-out infinite;">
                <img src="/stars.svg" alt="" class="mx-auto">
                <img v-if="dark" src="/img-pokeball-blue.png" alt="" class="mx-auto">
                <img  v-if="!dark" src="/img-pokeball-red.png" alt="" class="mx-auto">
              </div>

              <p class="mt-6 text-higher text-lg leading-8 text-gray-600 dark:text-white dark:opacity-75">
                Welcome to the ultimate companion for all Pokémon trainers! Our Pokédex app is your gateway to the fascinating world of Pokémon, providing you with a comprehensive and interactive digital Pokédex right at your fingertips.
              </p>
              <div class="mt-10 text-higher flex items-center justify-center gap-x-6">

                <div  style="animation: circle 75s ease-in-out infinite;"  class="absolute inset-y-0 left-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
                  <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-70 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(0 66%, 12% 30%, 15% 0%, 35% 45%, 85% 15%, 100% 15%, 48% 60%, 100% 49%, 100% 100%, 0 100%, 30% 90%, 19% 48%);" />
                  <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(0 66%, 12% 30%, 15% 0%, 35% 45%, 85% 15%, 100% 15%, 48% 60%, 100% 49%, 100% 100%, 0 100%, 30% 90%, 19% 48%);" />
                </div>
                <div style="animation: circle 50s ease-in-out infinite; " class="absolute inset-y-0 right-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
                  <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(6% 4%, 0 73%, 25% 100%, 11% 27%, 75% 30%, 53% 86%, 40% 59%, 25% 100%, 84% 97%, 79% 5%);" />
                  <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(6% 4%, 0 73%, 25% 100%, 11% 27%, 75% 30%, 53% 86%, 40% 59%, 25% 100%, 84% 97%, 79% 5%);" />
                </div>
                <div class="added-transition rounded-md bg-red-600  dark:bg-indigo-600 px-3.5 py-3.5 text-sm font-semibold hover:bottom-1 relative text-white shadow-sm hover:bg-red-700 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
                  <NuxtLink to="/login">
                    LogIn 
                  </NuxtLink>
                </div>
                <div class="added-transition rounded-md bg-red-600  dark:bg-indigo-600 px-3.5 py-3.5 text-sm font-semibold hover:bottom-1 relative text-white shadow-sm hover:bg-red-700 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
                  <NuxtLink to="/signup">
                    Create account
                  </NuxtLink>
                </div>
              </div>
            </div>
          </div>
          <div style="animation: circle 60s ease-in-out infinite;" class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
            <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
            <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
          </div>
        </div>
      </div>
          <div v-if="rickRolled" class="w-full h-full overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
            <div class="relative w-auto my-6 mx-auto max-w-6xl">
              <!--content-->
              <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                <!--header-->
                <div class="flex items-start justify-between p-5 border-b border-solid border-slate-200 rounded-t">
                  <h3 class="text-3xl font-semibold  dark:text-gray-900">
                    You are Rickrolled 🕺🏼
                  </h3>
                </div>
                <div class=" relative p-6 flex-auto">
                  <iframe class="rickVideo" width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ?controls=0?autoplay=1&enablejsapi=1&autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
                </div>
              </div>
            </div>
          </div>
          <div v-if="rickRolled" class="opacity-25 fixed inset-0 z-40 bg-black"></div>
    </section>
  </div>
</template>

<script setup lang="ts">

// data
const dark = useCookie<boolean>("dark");
const rickRolled = false;

// methods
function changeDarkMode(isDark: boolean): void {
  dark.value = isDark;
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
