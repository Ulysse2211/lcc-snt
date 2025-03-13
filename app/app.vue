<template>
  <div class="fixed top-0 left-0 w-screen z-50">
    <div class="relative overflow-hidden outline-gray-600 outline-2">
      <div class="bg-black opacity-25 blur-lg w-screen h-full absolute inset-0"></div>
      <nav class="flex items-center justify-between relative z-10 p-5">
        <img alt="Logo" src="assets/logo.svg" draggable="false" class="w-md" />
        <div class="flex items-center gap-14">
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
