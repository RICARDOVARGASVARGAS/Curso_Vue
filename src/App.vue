<script setup>

import { ref, reactive } from 'vue'

let users = [
  {
    id: 1,
    name: 'John Doe'
  },
  {
    id: 2,
    name: 'Mary Doe'
  },
  {
    id: 3,
    name: 'Jane Roe'
  },
  {
    id: 4,
    name: 'John Roe'
  }
]

</script>

<template>

  <ul>
    <li v-for="({ id, name }, index) in users" :key="id">
      {{ id }} - {{ name }}
    </li>
    -------------
    <template v-for="({ id, name }, index) in users" :key="id">
      <li>{{ id }} - {{ name }}</li>
    </template>

  </ul>

</template>

<style scoped></style>
