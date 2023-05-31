<script setup>
import TheWelcome from '../components/Inicio.vue'
</script>

<template>
  <main class="fondo">
    <TheWelcome />
  </main>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
.fondo
{
  background: linear-gradient(to bottom, #007bff5d -20%, #ffffff 100%);
  width: 100%;
  display: inline-flex;
}

</style>
