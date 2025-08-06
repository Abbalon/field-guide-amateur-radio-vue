<!-- src/components/PageTitle.vue -->
<template>
  <h1 class="page-title">{{ title }}</h1>
</template>

<script setup lang="ts">
// Define las propiedades que este componente espera recibir
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
})
</script>

<style scoped>
.page-title {
  font-family: 'CharcoalHandwriting', cursive;
  font-size: 2.5rem;
  text-align: center;
  color: #3b3a36;
  margin: 1.5rem 0;
}
</style>
