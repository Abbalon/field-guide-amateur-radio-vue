<template>
  <div class="page-content not-found">
    <h2 class="section-title">Lost in the Frequencies</h2>
    <p>
      It seems this entry has been torn from the notebook. The signal is lost.
      Perhaps you can return to the first page and try a different path.
    </p>
    <router-link to="/" class="notebook-link">
      <p>Return to the home page</p>
    </router-link>
  </div>
</template>

<style scoped>
.not-found {
  text-align: center;
  padding-top: 5rem;
}
</style>