<template>
  <div class="m-10 mr-15 ml-15">
    <div class="overflow-hidden rounded-lg flex justify-center items-center">
      <div class="blur-lg h-full w-full">
        <img alt="Logo" src="assets/hero.png" draggable="false" class="w-full" />
      </div>
      <div class="absolute inset-0 flex justify-center items-center z-10">
        <div class="mb-50">
          <h1 class="text-9xl text-red-700">Lycée Camille Claudel</h1>
          <span class="text-white text-2xl">Lycée des métiers des arts et du design</span>
        </div>
      </div>
    </div>
    <div class="grid grid-cols-1 gap-10 items-center mt-35 content-center">
      <UCard variant="soft" class="bg-slate-300">
        <div class="flex gap-20">
          <p>Le lycée est composé de cinq bâtiments où se déroulent les cours. Le premier compte quatre étages, le deuxième en a trois, tout comme le troisième et le quatrième, tandis que le dernier ne comporte que deux étages.
            <br><br>
            Au sein de ces bâtiments, vous trouverez également le CDI, la cantine, l'infirmerie, les bureaux administratifs, ainsi que la vie scolaire.
            <br><br>
            Le lycée Camille Claudel propose différentes filières :<br>
            - Filière générale, avec les spécialités : HGGSP, Mathématiques, Physique-Chimie, HLP, SES, NSI, Arts, Musique, SVT, etc.<br>
            - Filière technologique: STI2D, STMG, STI2A.<br>
            - Filière professionnelle : MARVI.</p>
          <img alt="Logo" src="assets/devanturelycee.png" draggable="false" class="w-md float-right rounded-xl" />
        </div>
      </UCard>
      <UCard variant="soft" class="bg-slate-300">
        <div class="flex gap-20">
          <img alt="Logo" src="assets/plan.png" draggable="false" class="w-md float-left rounded-xl" />
          <p>
            Le lycée est divisé en 5 batiments :<br>
            Blabla<br>
          </p>
        </div>
      </UCard>
      <div>
        <hr class="mb-15">
        <h1 class="text-5xl mb-15">Articles</h1>
        <div class="flex gap-20">
          <ULink class="outline rounded-xl w-80 bg-slate-300 hover:bg-slate-400" v-for="(post, index) in posts" :to="post.path">
            <img :src="post.image" alt="Image" draggable="false" class="rounded-t-xl w-full mb-5">
            <div class="m-5">
              <h1 class="text-3xl">{{ post.title }}</h1>
              <hr class="m-3">
              <h2>{{ post.description }}</h2>
            </div>
          </ULink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const { data: posts } = await useAsyncData('content', () => queryCollection('content').all())
</script>