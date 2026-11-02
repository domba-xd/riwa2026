<template>
  <q-page padding>
    <div class="q-pa-md" style="max-width: 400px">
  <q-form @submit="onSubmit" @reset="onReset" class="q-gutter-md">
    <q-input
      filled
      v-model="name"
      label="Korisničko ime *"

      lazy-rules
      :rules="[val => (val && val.length > 0) || 'Please type something']"
    />

    <q-input
      filled
      type="password"
      v-model.number="lozinka"
      label="Lozinka *"
      lazy-rules
      :rules="[
        val => (val && val.length > 0) || 'Kreirajte lozinku',
        val => (val && val.length > 3) || 'Lozinka mora sadržavati više od 4 znakova'

      ]"
    />


    <div>
      <q-btn label="Prijavi se" type="submit" color="primary" />
      <q-btn
        label="Reset"
        type="reset"
        color="primary"
        flat
        class="q-ml-sm"
      />
    </div>
  </q-form>
</div>
  </q-page>
</template>

<script setup>
import { useQuasar } from 'quasar'
import { ref } from 'vue'

const $q = useQuasar()

const name = ref(null)
const lozinka = ref(null)
const accept = ref(false)


function onReset() {
  name.value = null
  lozinka.value = null
  accept.value = false
}
</script>
