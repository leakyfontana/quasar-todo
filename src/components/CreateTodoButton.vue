<template>
  <q-btn @click="handleClick" />
</template>

<script setup>
import { useQuasar } from 'quasar'

const $q = useQuasar()

const handleClick = () => {
  $q.dialog({
    title: 'Create Todo',
    prompt: {
      model: '',
      type: 'text'
    }
  }).onOk(createTodo)
}

const createTodo = (data) => {
  $q.notify({
    message: `Todo created: ${data}`,
    icon: 'mdi-check',
    color: 'positive'
  })
}
</script>
