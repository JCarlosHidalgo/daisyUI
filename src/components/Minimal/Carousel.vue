<script setup>
import 'vue3-carousel/carousel.css'
import { ref } from 'vue'
import { Carousel, Slide } from 'vue3-carousel'

const props = defineProps({
    carouselHeight: Number,
    carouselImages: Array,
})

const carouselRef = ref()
const currentSlide = ref(1)

const next = () => carouselRef.value.next()
const prev = () => carouselRef.value.prev()

const images = Array.from({ length: 10 }, (_, index) => ({
    id: index + 1,
    url: `https://picsum.photos/seed/${Math.random()}/800/600`,
}))



const config = {
    height: props.carouselHeight,
    autoplay: 2000,
    itemsToShow: 1,
    gap: 5,
    slideEffect: 'slide',
    breakpointMode: 'carousel',
    breakpoints: {
        350: {
            itemsToShow: 1,
            snapAlign: 'center',
        },
        700: {
            itemsToShow: 2,
            snapAlign: 'start',
        },
        1200: {
            itemsToShow: 3,
            snapAlign: 'start'
        }
    },
    wrapAround: true
}
</script>

<template>
    <div class="space-y-3 flex flex-col items-center mx-3">
        <Carousel ref="carouselRef" v-model="currentSlide" v-bind="config">
            <Slide v-for="image in images" :key="image.id">
                <img :src="image.url" alt="image" />
            </Slide>
        </Carousel>
        <div class="join">
            <button @click="prev" class="btn join-item rounded-l-xl">
                <svg fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                    stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 19.5 3 12m0 0 7.5-7.5M3 12h18" />
                </svg>
            </button>
            <button @click="next" class="btn join-item rounded-r-xl">
                <svg fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                    stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5 21 12m0 0-7.5 7.5M21 12H3" />
                </svg>

            </button>
        </div>
    </div>

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
    object-fit: cover;
}
</style>