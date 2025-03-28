<template>
  <div class="mt-0 mb-2 w-120">
    <NuxtLink to="/">
      <img src="/assets/logoanim3_1.gif" alt="Luca School of Arts" class="animated-logo" />
    </NuxtLink>
  </div>
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  console.log("Component is geladen!");
});
</script>

<style scoped>
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animated-logo {
  width: 250px; /* Maak de GIF groter */
  height: auto;  /* Houd de verhoudingen correct */
  object-fit: contain;
  animation: fadeIn 1s ease-in-out;
  transform: translate(-20px, -10px); /* Verplaats naar links (-X) en omhoog (-Y) */
}
</style>

