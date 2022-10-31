<template>
  <div class="bg-hero h-screen bg-gray-700 text-gray-100 overflow-y-auto px-6 md:px-0">
    <div class="mx-auto block max-w-screen-md h-full">
      <!-- Page content -->
      <Nuxt />

      <!-- Footer -->
      <div class="mt-24 flex items-center justify-center pb-4 gap-2">
        <p class="text-xs font-light text-white opacity-60">Powered By</p>
        <img class="w-auto h-[18px] opacity-60" src="/pillar.svg">
      </div>
    </div>
  </div>
</template>

<style>
.bg-hero {
  background-image: url('/bg.jpeg');
}
</style>
