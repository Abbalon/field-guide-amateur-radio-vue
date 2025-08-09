<!-- src/components/Footer.vue -->
<template>
  <footer class="notebook-footer">
    <router-link v-if="route.name !== 'Home'" to="/" class="notebook-link">
      <p>
        Return to the home page
        <img src="@/assets/images/icons8-home.svg" alt="Home" class="home-icon" />
      </p>
    </router-link>
    <p>— 73s and clear skies, from the field.</p>
    <div class="author-signature"></div>
  </footer>
</template>

<script setup lang="ts">
import { useRoute } from 'vue-router'

defineOptions({
  name: 'NotebookFooter',
})
const route = useRoute()
</script>

<style scoped>
.notebook-footer {
  text-align: center;
  margin-top: 2rem;
  border-top: 2px dashed #9d9d9d;
  padding-top: 1rem;
  font-style: italic;
  position: relative; /* Para controlar el apilamiento */
  z-index: 1; /* Asegura que el footer esté por encima del lomo del libro */
}

.home-icon {
  width: 1em;
  height: 1em;
  vertical-align: middle;
  margin-left: 0.5em;
  background-color: #3b3a36;
}
</style>
