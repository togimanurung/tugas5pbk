<template>
  <q-card flat bordered class="my-card q-ma-sm" style="width: 250px">
    <q-img :src="img" :alt="name" style="height: 200px" />

    <q-card-section>
      <div class="text-subtitle1">{{ name }}</div>
      <div class="text-caption text-grey">Rp {{ price.toLocaleString() }}</div>
    </q-card-section>

    <q-card-actions align="right">
      <q-btn color="primary" label="Beli" @click="buy" />
    </q-card-actions>
  </q-card>
</template>

<script setup>
import { defineProps } from 'vue'
import { Notify } from 'quasar'

const props = defineProps({
  name: String,
  price: Number,
  img: String
})

const buy = () => {
  Notify.create({
    message: `${props.name} ditambahkan ke keranjang!`,
    color: 'positive',
    icon: 'shopping_cart'
  })
}
</script>
