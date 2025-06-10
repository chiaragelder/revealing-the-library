
<template>
  <div class="mt-0 mb-2 w-120">
    
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
  width: 100px;   /* vaste breedte */
  height: 50px;   /* vaste hoogte */
  object-fit: contain;
  animation: fadeIn 1s ease-in-out;
  transform: translate(-20px, -10px);
}
</style>


