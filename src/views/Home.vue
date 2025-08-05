<template>
  <div class="page-content">
    <div class="intro-note">
      <h2 class="section-title">First Entry</h2>
      <p>
        My fingers are cold, the air is crisp, and the transceiver is humming.
        This field guide is a chronicle of my journey into the world of amateur
        radio. Here, you'll find my scribbled notes on antennas, my maps of
        distant frequencies, and the schematics of my latest projects. Grab your
        gear, turn the page, and let's explore the airwaves together.
      </p>
    </div>

    <div class="navigation-links">
      <h3 class="section-subtitle">Topics</h3>
      <ul>
        <li><router-link to="/antennas" class="notebook-link">Antennas: The Art of Reaching Far</router-link></li>
        <li><router-link to="/equipment" class="notebook-link">Equipment: My Trusty Transceiver</router-link></li>
        <li><router-link to="/diy" class="notebook-link">DIY Projects: A Solder's Tale</router-link></li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
// No se necesita lógica en este componente por ahora.
</script>

<style scoped>
.intro-note {
  padding: 1rem;
  border-left: 5px solid #a87e50; /* Como una pequeña mancha de café en el borde */
}
.notebook-link {
  text-decoration: none;
  font-weight: bold;
  color: #3b3a36;
  position: relative;
  transition: transform 0.2s;
}
.notebook-link:hover {
  transform: translateX(5px); /* Efecto de que la página se mueve */
}
</style>