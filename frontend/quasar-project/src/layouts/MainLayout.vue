<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Knjižnica </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

        <EssentialLink
          v-for="link in linksList"
          :key="link.label"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import EssentialLink from '@/components/EssentialLink.vue'

const linksList = [
  {
    label: 'Popis Knjiga',
    caption: 'Ovdje se nalazi popis svih knjiga',
    icon: 'school',
    link: '/popis_knjiga'
  },
  {
    label: 'Pretraživanje',
    caption: 'Ovdje pretražujete knjige',
    icon: 'code',
    link: '/pretrazivanje'
  },
  {
    label: 'O nama',
    caption: 'ovdje se nalaze naše informacije',
    icon: 'chat',
    link: '/o_nama'
  },
  {
    label: 'Lokacija',
    caption: 'Naša lokacija',
    icon: 'record_voice_over',
    link: '/lokacija'
  },
  {
    label: 'Login',
    caption: 'Ovdje se Ulogirate',
    icon: 'rss_feed',
    link: '/login'
  },
  {
    label: 'Registracija',
    caption: 'Ovdje se registrirajte',
    icon: 'public',
    link: '/registracija'
  }
]

const leftDrawerOpen = ref(false)

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
