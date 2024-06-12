<template>
  <div  style="animation: circle 25s ease-in-out infinite;" class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-100" aria-hidden="true">
    <div v-if="!dark"  class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
    <div v-if="dark" class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#fff] to-[#4F46E5] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
  </div>
  <div  style="animation: circle 95s ease-in-out infinite;" class="absolute inset-x-0 -top-40 right-0 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-100" aria-hidden="true">
    <div v-if="!dark"  class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#f00] to-[#f00] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(50% 0%, 61% 35%, 100% 0, 65% 45%, 100% 100%, 49% 53%, 0 100%, 33% 46%, 0 0, 39% 35%);" />
    <div v-if="dark" class=" relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#fff] to-[#4F46E5] opacity-60 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(50% 0%, 61% 35%, 100% 0, 65% 45%, 100% 100%, 49% 53%, 0 100%, 33% 46%, 0 0, 39% 35%);)" />
  </div>
  <div style="animation: circle 60s ease-in-out infinite;" class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
    <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
    <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
  </div>
  <div  style="animation: circle 75s ease-in-out infinite;"  class="absolute inset-y-0 left-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
    <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-70 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(0 66%, 12% 30%, 15% 0%, 35% 45%, 85% 15%, 100% 15%, 48% 60%, 100% 49%, 100% 100%, 0 100%, 30% 90%, 19% 48%);" />
    <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(0 66%, 12% 30%, 15% 0%, 35% 45%, 85% 15%, 100% 15%, 48% 60%, 100% 49%, 100% 100%, 0 100%, 30% 90%, 19% 48%);" />
  </div>
  <div style="animation: circle 50s ease-in-out infinite; " class="absolute inset-y-0 right-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
    <div v-if="!dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff0000] to-[#ff0000] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(6% 4%, 0 73%, 25% 100%, 11% 27%, 75% 30%, 53% 86%, 40% 59%, 25% 100%, 84% 97%, 79% 5%);" />
    <div v-if="dark" class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#4F46E5] to-[#fff] opacity-50 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(6% 4%, 0 73%, 25% 100%, 11% 27%, 75% 30%, 53% 86%, 40% 59%, 25% 100%, 84% 97%, 79% 5%);" />
  </div>

</template>

<script setup lang="ts">
  const dark = useCookie<boolean>("dark");
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
</style>
