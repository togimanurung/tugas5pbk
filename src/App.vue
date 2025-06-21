<template>
  <q-layout view="lHh Lpr lFf">
    <MyNavbar />
    <q-page-container>
      <ProductGrid />
    </q-page-container>
    <MyFooter />
  </q-layout>
</template>

<script setup>
import MyNavbar from './components/MyNavbar.vue'
import ProductGrid from './components/ProductGrid.vue'
import MyFooter from './components/MyFooter.vue'
</script>
