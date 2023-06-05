<template>
  <q-layout view="hHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-toolbar class="bg-primary" />
        <q-item class="bg-grey-3">
          <q-item-section>
            Lists
          </q-item-section>
          <q-item-section side>
            <CreateTodoListButton
              icon="mdi-plus"
              flat
              round
              size="sm"
            />
          </q-item-section>
        </q-item>
        <TodoListsList />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import CreateTodoListButton from 'src/components/CreateTodoListButton.vue'
import TodoListsList from 'components/TodoListsList.vue'

/*
  drawer open
*/

const leftDrawerOpen = ref(false)

const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value
}

</script>
