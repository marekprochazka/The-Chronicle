<script setup lang="ts">
import { Card, CardContent, CardHeader } from '~/components/ui/card';

useHead({
  title: 'Home',
});

const bigMenu = [
  {
    title: 'TBD',
    image: '/assets/gifs/hello-there.webp',
    imgAlt: 'hello there obi wan kenobi',
    link: '/',
  },
];
</script>

<template>
  <div class="grid grid-cols-6 gap-4 p-2">
    <div v-for="item in bigMenu" :key="item.title" class="col-span-1">
      <NuxtLink :to="item.link">
        <Card>
          <CardHeader>
            <h1>{{ item.title }}</h1>
          </CardHeader>
          <CardContent>
            <img
                :alt="item.imgAlt"
                class="h-40 mx-auto w-full"
                :src="item.image"
            >
          </CardContent>
        </Card>
      </NuxtLink>
    </div>
  </div>
</template>