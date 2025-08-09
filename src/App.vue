<!-- src/App.vue -->
<template>
  <PageTitle title="Field Guide to Amateur Radio" />
  <div id="notebook-page">
    <Header />
    <main>
      <router-view v-slot="{ Component }">
        <transition name="page-turn" mode="out-in">
          <component :is="Component" />
        </transition>
      </router-view>
    </main>
    <Footer />
  </div>
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
  /* background-image: url('@/assets/images/notebook-lines.png'); Imagen de fondo con líneas de cuaderno */
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  min-height: 100vh;
  position: relative; /* Necesario para la transición y el lomo */
  perspective: 2500px; /* Crea el espacio 3D para el efecto de giro */
}

/* Lomo del libro simulado */
#notebook-page::before {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  left: 50%;
  width: 2px;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.15), rgba(0, 0, 0, 0));
  transform: translateX(-1px);
  z-index: 0;
}

main {
  position: relative; /* Asegura que el contenido esté por encima del lomo */
  z-index: 1;
}

/* Animación de paso de página */
.page-turn-enter-active,
.page-turn-leave-active {
  transition:
    opacity 0.5s,
    transform 0.5s;
}

.page-turn-enter-from {
  opacity: 0;
  transform: rotateY(-90deg);
  transform-origin: left;
}

.page-turn-leave-to {
  opacity: 0;
  transform: rotateY(90deg);
  transform-origin: right;
}
</style>
