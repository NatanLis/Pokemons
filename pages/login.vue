<template>
  <div :class="{ dark: dark }">
    <section class="App min-h-screen p-6 pb-0 lg:px-20 max-w-full overflow-x-hidden dark:text-white dark:bg-slate-900">
      <!-- header -->
      <header class="relative w-full flex justify-between items-center">
        <img src="/pokemon.svg" class="w-32" />
        <DarkMode @change="changeDarkMode" />
      </header>

      <div class="flex items-center justify-center text-not-that-higher mt-6 sm:mt-0">
        <div class="isolate lg:px-8">
          <div  style="animation: circle 55s ease-in-out infinite;" class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-100" aria-hidden="true">
            <div v-if="!dark"  class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
            <div v-if="dark" class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#fff] to-[#4F46E5] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
          </div>
          <div  style="animation: circle 95s ease-in-out infinite;" class="absolute inset-x-0 -top-40 right-0 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-100" aria-hidden="true">
            <div v-if="!dark"  class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#f00] to-[#f00] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(50% 0%, 61% 35%, 100% 0, 65% 45%, 100% 100%, 49% 53%, 0 100%, 33% 46%, 0 0, 39% 35%);" />
            <div v-if="dark" class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#fff] to-[#4F46E5] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(50% 0%, 61% 35%, 100% 0, 65% 45%, 100% 100%, 49% 53%, 0 100%, 33% 46%, 0 0, 39% 35%);)" />
          </div>

          <!-- login form -->
          <div class="flex items-center justify-center min-h-screen" style="width: 500px;">
            <form class="bg-white dark:bg-slate-800 p-8 rounded-lg shadow-lg w-full">
              <h2 class="text-3xl mb-6 text-center">Login</h2>

              <label class="block mb-4">
                <span class="text-gray-700 dark:text-white">Email</span>
                <input type="email" v-model="email" class="mt-1 block w-full p-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm dark:bg-slate-700" placeholder="you@example.com">
              </label>

              <label class="block mb-6">
                <span class="text-gray-700 dark:text-white">Password</span>
                <input type="password" v-model="password" class="mt-1 block w-full p-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm dark:bg-slate-700" placeholder="Enter your password">
              </label>

              <div class="flex justify-between items-center">
                <NuxtLink to="/">
                  <button type="button" @click="cancelLogin" class="py-2 px-4 bg-red-500 text-white rounded-lg hover:bg-red-600">Cancel</button>
                </NuxtLink>

                <button type="submit" @click="login" class="py-2 px-4 bg-blue-500 text-white rounded-lg hover:bg-blue-600">Login</button>

              </div>
            </form>
          </div>

          <div style="animation: circle 60s ease-in-out infinite;" class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
            <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
            <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
          </div>

          <div style="animation: circle 60s ease-in-out infinite;" class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
            <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
            <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
const email = ref('');
const password = ref('');
const router = useRouter()


function cancelLogin() {
  email.value = '';
  password.value = '';
}

function login() {
  // Add your login logic here
  console.log('Logging in with:', email.value, password.value);
  router.push("/pokemons")
  // router.push('/pokemons');

}

const dark = useCookie<boolean>("dark");

function changeDarkMode(isDark: boolean): void {
  dark.value = isDark;
}
</script>