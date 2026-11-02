<template>
  <q-page padding>
    <div class="text-h4 q-mb-sm">Popis svih knjiga</div>
    <p class="text-subtitle1">
      Ovdje se nalazi popis svih knjiga dostupnih u knjižnici, s podacima o autoru, godini izdanja i žanru.
    </p>

    <div class="q-pa-md">
  <q-table title="Treats" :rows="rows" :columns="columns" row-key="name" />
</div>
  </q-page>
</template>

<script setup>
  const columns = [
  {
    name:'id',
    label:'id',
    field:'id',
    align:'left',
    sortable: true,
    style: {
      fontSize:'14px'
    },
    headerStyle: {
      fontSize: '18px'
    },
    
  },
  {name:'naslov', label:'Naslov', field:'naslov', sortable: true},
  {name:'autor', label:'Autor', field:'autor', sortable: true},
  {name:'god_izd', label:'Godina Izdanja', field:'god_izd', sortable: true},
  {name:'dostupnost', label:'Dostupnost', field:'dostupnost', sortable: true}

]

const rows = [
  {
    id: 0,
    naslov: 'test',
    autor: 'test2',
    god_izd: '75556',
    dostupnost: 'dostupno'
  },
    {
    id: 1,
    naslov: 'test',
    autor: 'test2',
    god_izd: '6543',
    dostupnost: 'dostupno'
  },
    {
    id: 2,
    naslov: 'test',
    autor: 'test2',
    god_izd: '4455',
    dostupnost: 'dostupno'
  },
    {
    id: 3,
    naslov: 'test',
    autor: 'test2',
    god_izd: '2345',
    dostupnost: 'nedostupno'
  },
    {
    id: 4,
    naslov: 'test',
    autor: 'test2',
    god_izd: '1234',
    dostupnost: 'dostupno'
  },

]
</script>