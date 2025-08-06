<!-- src/components/Header.vue -->
<template>
  <header class="notebook-header">
    <div class="header-content">
      <h1 class="main-title">
        <span class="carbon-draw">Field Guide of an Amateur Radio</span>
      </h1>
      <p class="subtitle">Notes from the airwaves and beyond...</p>
    </div>
    <div class="radio-sketch">
      <svg width="100" height="100" viewBox="0 0 100 100"></svg>
    </div>
  </header>
</template>

<script setup lang="ts">
defineOptions({ name: 'AppHeader' })
// No se necesita lógica en este componente por ahora.
</script>

<style scoped>
.notebook-header {
  text-align: center;
  margin-bottom: 2rem;
  border-bottom: 2px dashed #9d9d9d; /* Borde que parece un desgarro de papel */
}
.main-title {
  font-family: 'HandDrawnTitle', serif; /* Fuente más gruesa para el título */
  font-size: 3rem;
  text-transform: uppercase;
}
.subtitle {
  font-style: italic;
  font-size: 1.2rem;
}
.radio-sketch {
  /* Estilo para el dibujo */
  position: absolute;
  top: 1rem;
  right: 1rem;
}
</style>
