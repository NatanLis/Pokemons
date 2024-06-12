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
          <div class="mx-auto max-w-2xl py-16 sm:py-24 lg:py-32">
            <div class="text-center">
              <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-7xl dark:text-white">
                Create Your Account
              </h1>
              <p class="mt-6 text-higher text-lg leading-8 text-gray-600 dark:text-white dark:opacity-75">
                Join the ultimate Pokémon trainers community by creating an account.
              </p>

              <form @submit.prevent="handleSubmit" class="mt-8 space-y-6">
                <div class="rounded-md shadow-sm -space-y-px">
                  <div>
                    <label for="email" class="sr-only">Email address</label>
                    <input id="email" name="email" type="email" required
                      class="relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-t-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm dark:bg-slate-800 dark:border-gray-700 dark:text-white"
                      placeholder="Email address">
                  </div>
                  <div>
                    <label for="password" class="sr-only">Password</label>
                    <input id="password" name="password" type="password" required
                      class="relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-b-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm dark:bg-slate-800 dark:border-gray-700 dark:text-white"
                      placeholder="Password">
                  </div>
                  <div>
                    <label for="confirm-password" class="sr-only">Confirm Password</label>
                    <input id="confirm-password" name="confirm-password" type="password" required
                      class="relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-b-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm dark:bg-slate-800 dark:border-gray-700 dark:text-white dark:bg-slate-800"
                      placeholder="Confirm Password">
                  </div>
                </div>

                <div class="mt-6 flex items-center justify-between">
                  <div class="flex items-center">
                    <input id="terms" name="terms" type="checkbox" required
                      class="h-4 w-4 text-indigo-600 focus:ring-indigo-500 border-gray-300 rounded dark:bg-slate-800 dark:border-gray-700">
                    <label for="terms" class="ml-2 block text-sm text-gray-900 dark:text-gray-400">
                      I agree to the terms and conditions
                    </label>
                  </div>
                </div>

                <div class="mt-6 flex justify-center">
                  <button type="submit"
                    class="added-transition rounded-md bg-red-600 dark:bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-red-700 dark:hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                    Create Account
                  </button>
                </div>
              </form>

              <p class="mt-6 text-sm text-gray-600 dark:text-gray-400">
                Already have an account?
                <NuxtLink to="/login" class="font-medium text-red-600 dark:text-indigo-600 hover:text-red-700 dark:hover:text-indigo-700">
                  Log in
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
const dark = useCookie<boolean>("dark");

function changeDarkMode(isDark: boolean): void {
  dark.value = isDark;
}
</script>
