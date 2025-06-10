<template>
  <div class="bg-white text-gray-900">
    <!-- Hero Section -->
    <section class="pl-16 md:pl-24 lg:pl-48 pr-4 py-10">
      <div class="container mx-auto flex items-start justify-center">
        <!-- Blok van afbeelding + tekst -->
        <div class="flex items-start mr-32">
          <!-- Grote Afbeelding links -->
          <img src="public/images/interfunktionen9 (1).png" alt="Book 4" class="w-48 h-72 object-cover mr-6" />

          <!-- Titel en tekst -->
          <div>
            <h1 class="text-3xl md:text-4xl font-bold text-black text-left pb-6 mt-4">
              Interfunktionen 1970, 4
            </h1>

            <p class="text-sm text-black italic lato-font">
              Published by Friedrich Wolfram Heubach, Cologne
            </p>

            <div class="max-w-prose">
              <div class="w-full mt-2 border-b border-gray-300"></div>

              <p class="text-sm text-black lato-font mt-4">
                Interfunktionen, an art journal which published 12 issues between 1968 and 1975 in Cologne, founded by Friedrich Wolfram (aka Fritz) Heubach and later edited by Benjamin H.D. Buchloh (nos. 11-12). It had been one of the most important European art magazines since World War II. Dissenting from the new ‘art-as-commodity’ attitude expressed at Arnold Bode’s documenta 4, Interfunktionen was an interdisciplinary effort among activist artists to promote European art and ideas without bowing to de commerciële trends.
              </p>

              <div class="w-full mt-2 border-b border-gray-300"></div>
            </div>

            <div class="grid grid-rows-2 grid-cols-2 gap-2 mt-2">
              <div class="text-sm font-regular text-black">
                <p>Author</p>
                <p>Release Date</p>
                <p>Format</p>
                <p>Features</p>
                <p>Language</p>
                <p>ISBN</p>
              </div>
              <div class="text-sm font-semibold text-black lato-font">
                <p>Adam Silver</p>
                <p>May 20, 2000</p>
                <p>21x5</p>
                <p>/</p>
                <p>English</p>
                <p>252720</p>
              </div>
            </div>
          </div>
        </div>

        <!-- You may also like -->
        <div class="flex flex-col space-y-4 border-l border-gray-300 pl-8">
          <p class="text-sm text-black font-semibold mb-4">You may also like</p>
          <img src="public/images/book1.jpg" alt="Book 5" class="w-24 h-36 object-cover rounded" />
          <img src="public/images/book2.jpg" alt="Book 2" class="w-24 h-36 object-cover rounded" />
          <img src="public/images/book3.jpg" alt="Book 3" class="w-24 h-36 object-cover rounded" />
          
        </div>
      </div>
    </section>

    <!-- Photo Grid Section -->
    <section class="px-16 md:px-32 lg:px-48 pt-2 pb-8 -mt-8">
      
      <div class="grid grid-cols-3 gap-4">
        <div v-for="(photo, index) in photos" :key="index">
          <img :src="photo" alt="Gallery Photo" class="object-cover w-full h-56" />
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { onMounted } from 'vue';

onMounted(() => {
  const link1 = document.createElement('link');
  link1.rel = 'stylesheet';
  link1.href = 'https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&display=swap';
  document.head.appendChild(link1);

  const link2 = document.createElement('link');
  link2.rel = 'stylesheet';
  link2.href = 'https://fonts.googleapis.com/css2?family=Lato:wght@400;700&display=swap';
  document.head.appendChild(link2);
});

const photos = [
  '/images/IMG_2004 kopie.JPG',
  '/images/IMG_2005 kopie.JPG',
  '/images/IMG_2009 kopie.JPG',
  '/images/IMG_2013 kopie.JPG',
  '/images/IMG_2111 kopie.JPG',
  '/images/IMG_2112 kopie.JPG'
];
</script>

<style scoped>
.playfair-font {
  font-family: 'Playfair Display', serif;
}

.lato-font {
  font-family: 'Lato', sans-serif;
}

img {
  border: 2px solid transparent;
  border-radius: 0px;
}

/* Flexbox */
.flex {
  display: flex;
  gap: 1rem;
}

.flex-col {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.border-l {
  border-left: 2px solid #ddd;
}

.pl-4 {
  padding-left: 1rem;
}
</style>
