<!-- src/App.vue -->
<template>
  <router-link to="/" class="notebook-link">
    <PageTitle title="Field Guide to Amateur Radio" />
    <div id="notebook-page">
      <Header />
      <main>
        <router-view></router-view>
      </main>
      <Footer />
    </div>
  </router-link>
</template>

<script setup lang="ts">
import PageTitle from './components/PageTitle.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
</script>

<style>
/* Estilos globales para la apariencia de cuaderno */
body {
  background-color: #f7f3e8; /* Tono de papel viejo */
  font-family: 'CharcoalHandwriting', cursive; /* Sugerencia: Busca una fuente gratuita */
  color: #3b3a36; /* Color de tinta oscura */
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#notebook-page {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem;
  background-image: url('/path/to/notebook-lines.png'); /* Imagen de fondo con líneas de cuaderno */
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  min-height: 100vh;
}
</style>
