<template>
  <q-page padding>
    <div class="text-h4 q-mb-sm">Pretraživanje knjiga</div>
    <p class="text-subtitle1">
      Upiši pojam, odaberi pretražuješ li po naslovu ili autoru i klikni na Traži.
    </p>
    <div style="width: 50vh;"><q-input
      filled
      v-model="ph"
      label="Unos"
      placeholder="Unesi Naslov ili Autor"
      :dense="dense"
    /></div>
    <div class="q-pa-md">
      <q-checkbox v-model="poNaslovu" label="Naslov"/>
      <q-checkbox v-model="poAutoru" label="Autor"/>
    </div>
      <q-btn color="primary" label="Pretraži" icon="search" />
        
  </q-page>
</template>

<script setup>
import { ref } from 'vue'


const poNaslovu =ref(false)
const poAutoru = ref(false)
</script>