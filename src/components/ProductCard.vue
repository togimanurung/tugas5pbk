<template>
  <q-card class="my-card q-ma-sm" flat bordered style="width: 250px">
    <q-img
      :src="img"
      :alt="name"
      style="height: 200px"
    />

    <q-card-section>
      <div class="text-subtitle1">{{ name }}</div>
      <div class="text-caption text-grey">Rp {{ price.toLocaleString() }}</div>
    </q-card-section>

    <q-card-actions align="right">
      <q-btn
        color="primary"
        icon="shopping_cart"
        label="Beli Sekarang"
        @click="buyProduct"
        class="q-mr-sm"
      />
    </q-card-actions>
  </q-card>
</template>

<script setup>
import { Notify } from 'quasar'
import { defineProps } from 'vue'

const props = defineProps({
  name: String,
  price: Number,
  img: String
})

const buyProduct = () => {
  Notify.create({
    message: `${props.name} berhasil ditambahkan ke keranjang!`,
    color: 'positive',
    icon: 'check_circle'
  })
}
</script>
