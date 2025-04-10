<script lang="ts" setup>
const route = useRoute()
const { data: page } = await useAsyncData(route.path, () => {
  return queryCollection('content').path(route.path).first()
})
</script>

<template>
  <div class="m-30">
    <NuxtLink to="/" class="fixed flex items-center gap-2 text-cyan-600 m-2 hover:text-cyan-400">
      <UIcon name="i-lucide-arrow-left" class="size-5" />
      <h1>Retour à l'accueil</h1>
    </NuxtLink>
    <div class="mb-5 flex">
      <img :src="page?.image" alt="Image" class="mr-10 mt-12 h-full max-h-80 rounded-xl">
      <div class="w-full">
        <div class="flex justify-between">
          <div>
            <h1 class="text-4xl font-bold font-serif underline">{{ page?.title }}</h1>
            <h3 class="mt-5 mb-5"> {{ page?.description }}</h3>
          </div>
          <div class="flex items-center gap-2">
            <UIcon name="i-lucide-calendar" class="size-5" />
            <h1>{{ page?.date }}</h1>
          </div>
        </div>
        <hr>
        <ContentRenderer v-if="page" :value="page" class="mt-10 content"/>
      </div>
    </div>
  </div>
</template>

<style>

.content h1 {
  color: var(--color-red-900);
  margin-bottom: 15px;
  font-size: var(--text-6xl); /* 1.5rem (24px) */
  line-height: var(--text-6xl--line-height); /* calc(2 / 1.5) */
}

.content h2 {
  color: var(--color-red-950);
  font-size: var(--text-4xl); /* 1.5rem (24px) */
  margin-bottom: 10px;
  line-height: var(--text-4xl--line-height); /* calc(2 / 1.5) */
}

.content h3 {
  margin-bottom: 5px;
  font-size: var(--text-2xl); /* 1.5rem (24px) */
  line-height: var(--text-2xl--line-height); /* calc(2 / 1.5) */
}

.content h4 {
  font-size: var(--text-xl); /* 1.5rem (24px) */
  line-height: var(--text-xl--line-height); /* calc(2 / 1.5) */
}

.content h5 {
  font-size: var(--text-lg); /* 1.5rem (24px) */
  line-height: var(--text-lg--line-height); /* calc(2 / 1.5) */
}

.content a {
  color: var(--color-red-900);
  text-decoration: underline;
}

.content a:hover {
  color: var(--color-red-950);
}

.content blockquote {
  background-color: var(--color-slate-300);
  border-left: 4px solid var(--color-red-900);
  padding: 10px;
  margin: 20px 0;
}

.content code,
.content pre {
  color: var(--color-slate-200);
  background-color: var(--color-slate-700);
  padding: 2px 4px;
  border-radius: 4px;
}

.content hr{
  border: 1px solid var(--color-slate-500);
  margin: 20px 0;
}

.content img {
  max-width: 100%;
  height: auto;
  border-radius: 15px;
}

.content il,
.content ul {
  list-style-type: disc;
  margin-left: 20px;
}

.content ol {
  list-style-type: decimal;
  margin-left: 20px;
}

.content table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  background-color: var(--color-slate-300);
  border: 1px solid var(--color-slate-500);
  border-radius: 8px;
}

.content th, .content td {
  padding: 12px 16px;
  border-bottom: 1px solid var(--color-slate-500);
  border-right: 1px solid var(--color-slate-500);
  text-align: left;
}

.content th {
  font-weight: bold;
}

.content tr td:last-child,
.content tr th:last-child {
  border-right: none;
}

.content tr:last-child td {
  border-bottom: none;
}

.content tr:hover {
  background-color: var(--color-slate-400);
}

</style>
