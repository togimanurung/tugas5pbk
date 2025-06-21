<template>
  <q-carousel animated v-model="slide" height="250px" arrows navigation infinite>
    <q-carousel-slide :name="1" img-src="https://picsum.photos/800/250?random=1" />
    <q-carousel-slide :name="2" img-src="https://picsum.photos/800/250?random=2" />
  </q-carousel>
</template>

<script setup>
import { ref } from 'vue'
const slide = ref(1)
</script>
