<template>
  <q-page
    class="row"
    padding
  >
    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input
          dense
          :model-value="search"
          class="full-width"
          borderless
          placeholder="search"
        >
          <template #append>
            <q-icon
              name="mdi-magnify"
            />
          </template>
        </q-input>
      </q-toolbar>
      <q-list bordered>
        <q-item>
          <q-item-section side>
            <q-checkbox :model-value="true" />
          </q-item-section>
          <q-item-section>
            Go Shopping
          </q-item-section>
          <q-item-section side>
            <q-btn
              flat
              round
              size="sm"
              icon="mdi-delete"
            />
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const search = ref('')
</script>
