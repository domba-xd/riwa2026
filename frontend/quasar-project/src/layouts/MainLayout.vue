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

        <q-toolbar-title class="text-h3 text-weight-bolder"> Razvoj Interaktivnih Web aplikacija - Vježba </q-toolbar-title>

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
    label: 'GitHub',
    caption: 'github.com/LeniJuresa',
    icon: 'code',
    link: 'https://github.com/lenijuresa'
  },
    {
    label: 'Popis knjiga',
    caption: 'knjige',
    icon: 'book',
    link: '#/popis_knjiga'
  },
      {
    label: 'Pretraživanje',
    caption: 'search',
    icon: 'search',
    link: '#/pretrazivanje'
  },
  {
    label: 'O nama',
    caption: 'about us',
    icon: 'person',
    link: '#/o_nama '
  },
  {
    label: 'Naša lokacija',
    caption: 'location',
    icon: 'map',
    link: '#/lokacija'
  },
  {
    label: 'Prijava',
    caption: 'login',
    icon: 'login',
    link: '#/login'
  },
  {
    label: 'Registracija',
    caption: 'register',
    icon: 'account_box',
    link: '#/registracija'
  },
]

const leftDrawerOpen = ref(false)

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
