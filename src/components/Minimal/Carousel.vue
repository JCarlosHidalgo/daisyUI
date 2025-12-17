<script setup>
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

const images = Array.from({ length: 10 }, (_, index) => ({
  id: index + 1,
  url: `https://picsum.photos/seed/${Math.random()}/800/600`,
}))

const config = {
  height: 300,
  itemsToShow: 2,
  gap: 5,
}
</script>

<template>
  <Carousel v-bind="config">
    <Slide v-for="image in images" :key="image.id">
      <img :src="image.url" alt="image" />
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
</template>

<style>
.carousel {
  --vc-pgn-background-color: white;
  --vc-nav-background: var(--color-base-200);
  --vc-nav-border-radius: 100%;
}
img {
  border-radius: 8px;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>