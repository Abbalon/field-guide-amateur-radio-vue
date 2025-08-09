<!-- src/views/Home.vue -->
<template>
  <div class="page-content">
    <div class="intro-note">
      <h2 class="section-title">First Entry</h2>
      <p>
        My fingers are cold, the air is crisp, and the transceiver is humming. This field guide is a
        chronicle of my journey into the world of amateur radio. Here, you'll find my scribbled
        notes on antennas, my maps of distant frequencies, and the schematics of my latest projects.
        Grab your gear, turn the page, and let's explore the airwaves together.
      </p>
    </div>

    <div class="navigation-links">
      <h3 class="section-subtitle">Topics</h3>
      <ul>
        <li>
          <router-link to="/antennas" class="notebook-link"
            >Antennas: The Art of Reaching Far</router-link
          >
        </li>
        <li>
          <router-link to="/equipment" class="notebook-link"
            >Equipment: My Trusty Transceiver</router-link
          >
        </li>
        <li>
          <router-link to="/regulations" class="notebook-link"
            >Regulations: Navigating the Rules</router-link
          >
        </li>
        <li>
          <router-link to="/diy" class="notebook-link">DIY Projects: A Solder's Tale</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
defineOptions({ name: 'HomePage' })
// No se necesita lógica en este componente por ahora.
</script>

<style scoped>
.intro-note {
  padding: 1rem;
  border-left: 5px solid #a87e50; /* Como una pequeña mancha de café en el borde */
  margin-bottom: 2rem;
}
.notebook-link {
  text-decoration: none;
  font-weight: bold;
  color: #3b3a36;
  position: relative;
  transition: all 0.2s ease-in-out;
  display: inline-block; /* Para que el transform funcione correctamente */
  padding: 8px 12px;
}
.notebook-link:hover {
  transform: translateX(10px); /* Efecto de que la página se mueve */
  color: #a87e50;
}

.navigation-links ul {
  list-style: none;
  padding-left: 30px; /* Espacio para las pestañas */
}

.navigation-links li {
  margin: 1rem 0;
}

/* Simula una pestaña de marcador de página */
.notebook-link::before {
  content: '';
  position: absolute;
  left: -30px;
  top: 50%;
  transform: translateY(-50%);
  width: 20px;
  height: 30px;
  background-color: #d1c1a9;
  border: 1px solid #a87e50;
  border-right: none;
  border-radius: 5px 0 0 5px;
  box-shadow: -2px 2px 4px rgba(0, 0, 0, 0.1);
  transition: all 0.2s ease-in-out;
}

.notebook-link:hover::before {
  background-color: #a87e50;
  transform: translateY(-50%) translateX(-5px);
}
</style>
