<template>
  <q-page padding>
    <div class="text-h4 q-mb-sm">Registracija</div>
    <p class="text-subtitle1">
      Ispuni podatke za izradu novog korisničkog računa u knjižnici.
    </p>

    <div class="q-pa-md" style="max-width: 500px">
      <q-form @submit.prevent="potvrdi" class="q-gutter-md">
        <q-input v-model="korisnik.ime" label="Ime" outlined />
        <q-input v-model="korisnik.prezime" label="Prezime" outlined />
        <q-input v-model="korisnik.email" label="Email" type="email" outlined />
        <q-input v-model="korisnik.korisnicko_ime" label="Korisničko ime" outlined />
        <q-input v-model="korisnik.lozinka" label="Lozinka" type="password" outlined />

        <q-btn type="submit" color="primary" label="Potvrdi" no-caps />
      </q-form>
    </div>
  </q-page>
</template>

<script setup>
import { reactive } from 'vue'

const korisnik = reactive({
  ime: '',
  prezime: '',
  email: '',
  korisnicko_ime: '',
  lozinka: ''
})

function potvrdi () {
  console.log('Registracija:', { ...korisnik })
}
</script>