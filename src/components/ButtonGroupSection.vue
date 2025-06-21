<template>
  <div class="q-pa-xl q-gutter-md column items-center bg-grey-1 rounded-borders shadow-1">
    <div class="text-h5 text-primary">Fitur Interaktif</div>

    <q-btn-group push>
      <q-btn label="Alert" icon="warning" @click="showAlert" />
      <q-btn label="Log" icon="code" @click="logConsole" />
      <q-btn label="Jam" icon="schedule" @click="showTime" />
    </q-btn-group>

    <q-btn-group outline>
      <q-btn outline color="teal" label="Halo" @click="sayHello" />
      <q-btn outline color="indigo" label="Terima Kasih" @click="sayThanks" />
    </q-btn-group>

    <q-btn-group rounded>
      <q-btn color="purple" glossy icon="favorite" @click="like" />
      <q-btn color="orange" glossy icon="shopping_cart" @click="buy" />
      <q-btn color="blue" glossy icon="share" @click="share" />
    </q-btn-group>
  </div>
</template>

<script setup>
import { Notify } from 'quasar'

const showAlert = () => {
  Notify.create({ color: 'negative', message: 'Ini alert penting!', icon: 'error' })
}
const logConsole = () => {
  console.log('Log dari tombol.')
}
const showTime = () => {
  Notify.create(`Sekarang jam: ${new Date().toLocaleTimeString()}`)
}
const sayHello = () => {
  Notify.create('Halo 👋')
}
const sayThanks = () => {
  Notify.create('Terima kasih 🙏')
}
const like = () => {
  Notify.create('Kamu menyukai produk ini ❤️')
}
const buy = () => {
  Notify.create('Masuk ke keranjang 🛒')
}
const share = () => {
  Notify.create('Link produk telah dibagikan 🔗')
}
</script>
