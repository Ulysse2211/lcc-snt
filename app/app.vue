<template>
  <div class="fixed top-0 left-0 w-screen z-50">
    <div class="relative overflow-hidden outline-gray-600 outline-2">
      <div class="bg-black opacity-25 blur-lg w-screen h-full absolute inset-0"></div>
      <nav class="flex items-center justify-between relative z-10 p-5">
        <img alt="Logo" src="assets/logo.svg" draggable="false" class="w-md" />
        <div class="absolute left-130">
          <a href="tel:+33134211893" class="flex items-center gap-2 m-2 hover:text-white">
            <UIcon name="i-lucide-phone" class="size-5" />
            <h1>+33 1.34.21.18.93</h1>
          </a>

          <a href="mailto:0951710t@ac-versailles.fr" class="flex items-center gap-2 m-2 hover:text-white">
            <UIcon name="i-lucide-mail" class="size-5" />
            <h1>0951710t@ac-versailles.fr</h1>
          </a>
        </div>
        <div class="flex items-center gap-14 mr-10">
          <UButton
              href="https://0951710t.index-education.net/pronote/">
            <div class="flex items-center">
              <img
              src="assets/PRONOTE-papillon.svg"
              draggable="false"
              class="w-10"/>
              <h1 class="ml-5 text-2xl">Pronote</h1>
            </div>
            </UButton>
          <UButton
              href="https://psn.monlycee.net/cas/init?redirectUrl=https://psn.monlycee.net/">
            <div class="flex items-center">
            <img
                src="assets/monlycee.png"
                draggable="false"
                class="w-10 rounded"/>
            <h1 class="ml-5 text-2xl">Monlycée</h1>
          </div>
          </UButton>
        </div>
      </nav>
    </div>
  </div>

  <div class="pt-20">
    <UApp>
      <NuxtPage />
    </UApp>
  </div>
</template>

<script setup lang="ts">
</script>
