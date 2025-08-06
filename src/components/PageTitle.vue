<!-- src/components/PageTitle.vue -->
<script setup lang="ts">
import { onMounted, watch } from 'vue'

const props = defineProps<{
  title: string
  required: true
  default: 'Field Guide to Amateur Radio'
  type: string
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

<!-- src/components/PageTitle.vue -->
<template>
  <h1 class="page-title">{{ title }}</h1>
</template>

<style scoped>
.page-title {
  font-family: 'CharcoalHandwriting', cursive;
  font-size: 2.5rem;
  text-align: center;
  color: #3b3a36;
  margin: 1.5rem 0;
}
</style>
