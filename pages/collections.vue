<template>
  <div class="min-h-screen bg-white text-gray-900">
    <!-- Hero Section -->
    <section class="px-12 md:px-28 py-10">
      <h1 class="text-3xl md:text-4xl font-bold text-black text-right pb-6 mt-4 font-playfair">
        Special collections <br>
      </h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10 mt-6">
        <div class="order-2 md:order-1">
              <a href="/overvieuwHubert" class="text-2xl font-bold text-black pb-4 font-lato cursor-pointer hover:underline inline-block">
                Hubert Peeters
              </a>
          <p class="text-base md:text-lg leading-relaxed">
            Hubert Peeters'  collection was one of the first Pop Art collections in the 1960s and gradually grew into one of the most important in Europe. The collection also includes an impressive selection of artists’ books and catalogues. In 2024, several hundred books — often signed by the artists and containing personal inscriptions to the doctor and his wife — were donated to the Sint-Lukas Library by Agnès Peeters-Rammant, daughter of Marie-Thérèse en Hubert Peeters.
            <br><br>
          </p>
        </div>
        <div class="w-full h-64 flex items-center justify-end order-1 md:order-2">
          <img src="public/images/Hubert.png" alt="Hubert Peeters Collection"
            class="object-contain max-w-full max-h-full" />
        </div>
      </div>
    </section>

    <!-- Photo Grid Section -->
    <section class="px-24 md:px-64 py-10">
      <h2 class="text-2xl font-bold text-blue-900 pb-6 font-playfair"></h2>

      <div class="grid grid-cols-3 gap-x-2 gap-x-2">
        <div
          v-for="(photo, index) in photos"
          :key="index"
          class="h-56"
        >
          <img :src="photo" :alt="'Photo ' + (index + 1)" class="object-cover w-full h-full rounded" />
        </div>
      </div>
    </section>
  </div>

  
  <section class="px-12 md:px-28 py-40">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-10 mt-6">
      <div class="order-2 md:order-1">
        <h2 class="text-2xl font-bold text-black pb-4 font-lato">Dirk Lauwaert</h2>
        <p class="text-base md:text-lg leading-relaxed">
          Dirk Lauwaert was an exceptional lecturer, one of the most important writers on culture in this country, and a very kind and generous man. His library contained more than seven thousand titles on film, photography, visual arts, architecture, urban planning, semiotics, philosophy, and more. After his passing, the collection was entrusted by his family to the Sint-Lukas Library in Brussels, with the explicit wish that it be made accessible to students and researchers.
          In 2023, Sophie Nys, together with the librarians, designed a space in the library to present books from the Lauwaert collection. At regular intervals, a reader is invited to make a personal selection from the Lauwaert library.
          The inventory of this extensive book collection can be viewed via this link. Titles from the collection can be requested and consulted on site.
        </p>
      </div>
      <div class="w-full h-64 flex items-center justify-end order-1 md:order-2">
        <img src="public/images/Hubert.png" alt="Hubert Peeters Collection"
          class="object-contain max-w-full max-h-full" />
      </div>
    </div>
  </section>

  <!-- Photo Grid Section -->
  <section class="px-24 md:px-64 py-2">
    <h2 class="text-2xl font-bold text-blue-900 pb-6 font-playfair"></h2>

    <div class="grid grid-cols-3 gap-2">
      <div
        v-for="index in 6"
        :key="index"
        class="bg-gray-300 h-56 "
      ></div>
    </div>
  </section>
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
/* Playfair Display font toevoegen */
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap');

.font-playfair {
  font-family: 'Playfair Display', serif;
}

img {
  object-fit: contain;
}
</style>
