<template>
  <q-page
    class="row"
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
      <TodosList bordered />
    </q-card>
    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <CreateTodoButton
          fab
          style="margin-bottom: -42px;"
          class="q-ml-md"
          color="secondary"
          icon="mdi-plus"
        />
      </q-toolbar>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'
import CreateTodoButton from 'components/CreateTodoButton.vue'
import TodosList from 'components/TodosList.vue'

const search = ref('')
</script>
