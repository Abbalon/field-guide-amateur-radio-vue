<!-- src/components/PageTitle.vue -->
<script setup lang="ts">
import { onMounted, watch } from 'vue'

const props = defineProps<{
  title: string
}>()

onMounted(() => {
  document.title = props.title
})

watch(
  () => props.title,
  (newTitle) => {
    document.title = newTitle
  },
)
</script>

<template>
  <span style="display: none"
    ><!-- Este componente no renderiza nada en el DOM, solo actualiza el título del documento. --></span
  >
</template>
