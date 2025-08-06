<!-- src/views/Regulations.vue -->
<template>
  <div class="page-content">
    <div class="intro-note">
      <h2 class="section-title">Regulations: A Guide to the Rules</h2>
      <p>
        Just as a compass guides a traveler, regulations guide the radio amateur. Understanding the
        rules is not just a formality; it's a cornerstone of responsible and safe communication.
        Here are some notes on the key regulations that keep our airwaves clear and our hobby
        thriving.
      </p>
    </div>

    <div class="regulations-list">
      <h3 class="section-subtitle">Key Regulations</h3>
      <ul>
        <li>
          <h4>Licensing and Call Signs</h4>
          <p>
            Your license is your passport to the airwaves. It grants you the right to operate and
            assigns you a unique call sign, which is your identity on the radio. Always transmit
            your call sign at the beginning and end of each contact.
          </p>
        </li>
        <li>
          <h4>Frequency Allocation</h4>
          <p>
            The radio spectrum is a shared resource. Certain frequencies are allocated for specific
            uses. Operating on the correct band for your license class and purpose is crucial. This
            prevents interference and ensures a harmonious environment for all users.
          </p>
        </li>
        <li>
          <h4>Prohibited Communications</h4>
          <p>
            Avoid transmitting music, commercial messages, or profanity. Amateur radio is a
            non-commercial service for self-training, intercommunication, and technical
            investigation. Keep your messages personal, informative, and respectful.
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
// Por ahora, no se necesita lógica de JavaScript en este componente.
defineOptions({ name: 'RegulationsPage' })
</script>

<style scoped>
.page-content {
  /* Estilos para el contenedor de la página, similar a Home.vue */
  padding: 1rem;
}

.intro-note {
  padding: 1rem;
  border-left: 5px solid #a87e50;
  margin-bottom: 2rem;
}

.section-title {
  font-size: 2rem;
  font-weight: bold;
  color: #3b3a36;
}

.section-subtitle {
  font-size: 1.5rem;
  color: #5d5c58;
  border-bottom: 2px dashed #d1c1a9;
  padding-bottom: 0.5rem;
  margin-top: 2rem;
}

.regulations-list ul {
  list-style-type: none;
  padding: 0;
}

.regulations-list li {
  background-color: #fcf8ee;
  border-radius: 8px;
  padding: 1rem;
  margin-bottom: 1rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.regulations-list h4 {
  font-size: 1.2rem;
  color: #2c3e50;
  margin-top: 0;
}

.regulations-list p {
  line-height: 1.6;
}
</style>
