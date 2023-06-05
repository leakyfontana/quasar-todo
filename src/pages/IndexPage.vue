<template>
  <q-page padding>
    <q-select
      v-model="selected"
      filled
      :options="['X', 'C', 'B', 'S']"
    />
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const selected = ref(null)
</script>
