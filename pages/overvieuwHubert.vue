<template>
    <div>
      <template v-if="currentPage === 'overview'">
        <!-- Jouw eerste pagina: overzicht -->
        <div class="min-h-screen bg-white text-gray-900 px-12 md:px-28 py-12">
          <section class="flex justify-end items-center gap-10 mb-12">
            <div class="text-right max-w-md">
              <h1 class="text-4xl font-playfair font-bold">Special collection</h1>
              <h2 class="text-2xl font-playfair mt-2">- Hubert Peeters</h2>
            </div>
            <div class="w-64 h-64">
              <img 
                src="/images/Hubert.png" 
                alt="Hubert Peeters" 
                class="object-contain w-full h-full"
              />
            </div>
          </section>
      
          <section class="grid grid-cols-3 gap-5 ml-48 mr-48">
            <div 
              v-for="(photo, index) in photos" 
              :key="index" 
              class="flex flex-col items-center justify-center overflow-hidden bg-gray-100 p-2"
              :class="photo.route ? 'cursor-pointer' : ''"
            >
              <img 
                :src="photo.src" 
                :alt="photo.title" 
                :class="[
                  'object-contain w-auto transition-transform duration-300 hover:scale-105',
                  photo.maxH || 'max-h-56',
                  photo.route ? 'hover:cursor-pointer' : ''
                ]"
              />
              <p 
                v-if="photo.title === 'Interfunktionen'"
                class="mt-2 text-center text-sm text-black font-medium cursor-pointer"
                @click="goToBookPage"
              >
                {{ photo.title }}
              </p>
              <p 
                v-else
                class="mt-2 text-center text-sm text-black font-medium"
              >
                {{ photo.title }}
              </p>
            </div>
          </section>
        </div>
      </template>
  
      <template v-else-if="currentPage === 'bookpage'">
        <!-- De bookpage.vue inhoud hier inline -->
        <div class="bg-white text-gray-900">
          <!-- Hero Section -->
          <section class="pl-16 md:pl-24 lg:pl-48 pr-4 py-10">
            <div class="container mx-auto flex items-start justify-center">
              <div class="flex items-start mr-32">
                <img src="/images/interfunktionen9 (1).png" alt="Book 4" class="w-48 h-72 object-cover mr-6" />
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
                      Interfunktionen, an art journal which published 12 issues between 1968 and 1975 in Cologne...
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
              <div class="flex flex-col space-y-4 border-l border-gray-300 pl-8">
                <p class="text-sm text-black font-semibold mb-4">You may also like</p>
                <img src="/images/book1.jpg" alt="Book 5" class="w-24 h-36 object-cover rounded" />
                <img src="/images/book2.jpg" alt="Book 2" class="w-24 h-36 object-cover rounded" />
                <img src="/images/book3.jpg" alt="Book 3" class="w-24 h-36 object-cover rounded" />
              </div>
            </div>
          </section>
          <section class="px-16 md:px-32 lg:px-48 pt-2 pb-8 -mt-8">
            <div class="grid grid-cols-3 gap-4">
              <div v-for="(photo, index) in bookPhotos" :key="index">
                <img :src="photo" alt="Gallery Photo" class="object-cover w-full h-56" />
              </div>
            </div>
          </section>
          <button @click="goBack" class="m-8 px-4 py-2 bg-gray-200 rounded hover:bg-gray-300">Back</button>
        </div>


      </template>
    </div>
    <!-- Footer -->
    <div class="footer mt-12 pt-4 pb-4">
      <div class="footer-line mb-4"></div>
      <div class="flex justify-end mt-4 pr-8">
        <p class="footer-text lato-regular text-right">
          Luca School of Arts<br>
          Paleizenstraat 70, 1030 Brussel<br>
          bibliotheek.sintlukas@luca-arts.be<br>
          +32 3 250 11 33
        </p>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const currentPage = ref('overview');
  
  const photos = [
    { src: '/images/christo kopie.png', maxH: 'max-h-56', title: 'Christo' },
    { src: '/images/interfunktionen9 kopie.png', maxH: 'max-h-48', route: '/interfunktionen', title: 'Interfunktionen' },
    { src: '/images/Joseph Beuys und die Medizin kopie.png', title: 'Joseph Beuys' },
    { src: '/images/Neue Galerie der Stadt Aachen kopie.png', title: 'Neue Galerie Aachen' },
    { src: '/images/Tableau bon levain kopie.png', maxH: 'max-h-48', title: 'Tableau Bon Levain' },
    { src: '/images/telephonebook kopie.png', title: 'Telephonebook' },
    { src: '/images/The Fourth Sex Adolescent Extremes kopie.png', title: 'The Fourth Sex' },
    { src: '/images/Store days documents from The store and Ray Gun Theater kopie.png', title: 'Store Days' },
    { src: '/images/Gordon Matta-Clark One for all - all for one_ kopie.png', title: 'Gordon Matta-Clark' },
    { src: '/images/Roy Lichtenstein drawings and prints kopie.png', title: 'Roy Lichtenstein' },
    { src: '/images/sonsbeek 72 kopie.png', maxH: 'max-h-40', title: 'Sonsbeek 72' },
    { src: '/images/photo12.jpg', title: 'Photo 12' },
  ];
  
  const bookPhotos = [
    '/images/IMG_2004 kopie.JPG',
    '/images/IMG_2005 kopie.JPG',
    '/images/IMG_2009 kopie.JPG',
    '/images/IMG_2013 kopie.JPG',
    '/images/IMG_2111 kopie.JPG',
    '/images/IMG_2112 kopie.JPG'
  ];
  
  function goToBookPage() {
    currentPage.value = 'bookpage';
  }
  
  function goBack() {
    currentPage.value = 'overview';
  }
  </script>
  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap');
  .font-playfair {
    font-family: 'Playfair Display', serif;
  }
  .lato-font {
    font-family: 'Lato', sans-serif;
  }
  </style>
  