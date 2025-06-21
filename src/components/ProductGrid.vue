<template>
  <div class="q-pa-md bg-grey-1">
    <div class="text-h5 text-center text-primary q-mb-md">🧥 Koleksi Terbaru</div>
    <div class="row justify-center q-gutter-md">
      <ProductCard
        v-for="(item, index) in products"
        :key="index"
        :name="item.name"
        :price="item.price"
        :img="item.img"
      />
    </div>
  </div>
</template>

<script setup>
import ProductCard from './ProductCard.vue'

const products = [
  {
    name: 'Kaos Lengan Pendek',
    price: 120000,
    img: 'https://images.unsplash.com/photo-1521572163474-6864f9cf17ab'
  },
  {
    name: 'Jaket Hoodie',
    price: 250000,
    img: 'https://images.unsplash.com/photo-1618354691373-36b26d61c54c'
  },
  {
    name: 'Kemeja Kasual',
    price: 180000,
    img: 'https://images.unsplash.com/photo-1520975918313-60f7a56a4345'
  }
]
</script>
