<template>
    <div class="fixed top-0 left-0 w-screen z-50">
      <div class="relative overflow-hidden outline-gray-600 outline-2  backdrop-blur-lg">
        <div class="bg-red-300 opacity-30 blur-lg w-screen h-full absolute inset-0"></div>
        <nav class="flex items-center relative z-10 p-5">
          <img alt="Logo" src="assets/logo.svg" draggable="false" width="150" />
          <div class="flex place-self-center gap-10 ml-20">
            <a href="tel:+33134211893" class="flex items-center gap-2 hover:text-white">
              <UIcon name="i-lucide-phone" class="size-5" />
              <h1>+33 1.34.21.18.93</h1>
            </a>

            <a href="mailto:0951710t@ac-versailles.fr" class="flex items-center gap-2 hover:text-white">
              <UIcon name="i-lucide-mail" class="size-5" />
              <h1>0951710t@ac-versailles.fr</h1>
            </a>
          </div>
          <div class="absolute right-0 flex items-center gap-14 mr-10">
            <UButton
                href="https://0951710t.index-education.net/pronote/">
              <div class="flex items-center">
                <img
                    src="assets/pronote.svg"
                    draggable="false"
                    class="w-5"/>
                <h1 class="ml-5 text-xl">Pronote</h1>
              </div>
            </UButton>
            <UButton
                href="https://psn.monlycee.net/cas/init?redirectUrl=https://psn.monlycee.net/">
              <div class="flex items-center">
                <img
                    src="assets/monlycee.png"
                    draggable="false"
                    class="w-5 rounded"/>
                <h1 class="ml-5 text-xl">Monlycée</h1>
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

<style>
body{
  background-color: var(--color-slate-200);
}
</style>