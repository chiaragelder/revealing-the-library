<template>
  <div class="w-full container">
    <p class="pageTitle playfair-display text-3xl font-bold mb-10">
      All Books:
    </p>
    
    <ul class="w-full">
      <li v-for="book in books" :key="book.id" class="mb-6 w-full">
        <!-- Hier is de scheidingslijn -->
        <hr class="border-t-2 border-black mb-4 w-full block" />

        <div class="text-xl font-bold">
          <RouterLink :to="`/books/${book.id}`">
            {{ book.title }}
          </RouterLink>
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const books = ref([]);

onMounted(async () => {
  try {
    const response = await fetch('/data/books.json');
    const data = await response.json();
    books.value = data.map(book => ({
      id: book.id,
      title: book.title
    }));
  } catch (error) {
    console.error('Error fetching data:', error);
  }
});
</script>

<style>
.playfair-display {
  font-family: "Playfair Display", serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}
</style>

  