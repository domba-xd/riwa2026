<template>
  <q-page padding>
    <!-- content -->
     <div class="q-pa-md flex flex-center">
  <q-circular-progress
    :value="value"
    size="50x"
    color="green"
    class="q-ma-md"
  />

  <q-circular-progress
    :value="value"
    size="90px"
    :thickness="0.2"
    color="red"
    center-color="yellow"
    track-color="transparent"
    class="q-ma-md"
  />

  <q-circular-progress
    :value="value"
    size="45px"
    :thickness="19"
    color="blue"
    track-color="orange"
    class="q-ma-md"
  />

  <q-circular-progress
    :value="value"
    size="50px"
    :thickness="0.22"
    color="orange"
    track-color="grey-3"
    class="q-ma-md"
  />

  <q-circular-progress
    :value="value"
    size="120px"
    :thickness="0.6"
    color="black"
    center-color="red"
    class="q-ma-md"
  />

  <q-circular-progress
    :value="value"
    size="40px"
    :thickness="0.4"
    color="orange"
    track-color="grey-3"
    center-color="grey-8"
    class="q-ma-md"
  />
</div>
  </q-page>
</template>

<script setup>
const value = 71
</script>
