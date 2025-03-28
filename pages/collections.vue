<template>
  <div class="min-h-screen bg-white text-gray-900">
    <!-- Hero Section -->
    <section class="px-2 md:px-4 py-10"> <!-- Verlaag de padding van de zijkanten -->
      <h1 class="text-3xl md:text-4xl font-bold text-blue-900 text-right pb-6 mt-4">
        Special collection <br>
        <span class="text-2xl md:text-3xl">- Dirk Lauwaert</span>
      </h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10 mt-6">
        <div class="order-2 md:order-1">
          <p class="text-base md:text-lg leading-relaxed">
            <strong>Dirk Lauwaert</strong> was an exceptional teacher, one of the greatest writers on culture in our language area, and a truly kind and generous man.
            His book collection consists of approximately eight thousand titles on film, photography, visual arts, architecture, urban planning, semiotics, philosophy, and more.
            <br><br>
            In 2015, his family entrusted his collection to Sint-Lukas Brussels, with the explicit wish that it be made accessible to researchers.
          </p>
        </div>
        <div class="w-full h-64 flex items-center justify-end order-1 md:order-2">
          <img src="/images/dirk-lauweart.png" alt="Dirk Lauwaert Collection" 
            class="object-contain max-w-full max-h-full" />
        </div>
      </div>
    </section>

    <!-- Filters -->
    <div class="flex flex-wrap justify-center gap-4 md:gap-10 py-6 border-b">
      <select class="border px-4 py-2 rounded">
        <option>Author</option>
      </select>
      <select class="border px-4 py-2 rounded">
        <option>Language</option>
      </select>
      <select class="border px-4 py-2 rounded">
        <option>Format</option>
      </select>
    </div>

    <!-- Book Grid -->
    <section class="px-2 md:px-4 py-10"> <!-- Verlaag de padding van de zijkanten -->
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <!-- Dynamically load images for books -->
        <div v-for="n in 6" :key="n" class="border bg-gray-200 flex items-center justify-center p-2 rounded-lg h-64">
          <img :src="'/images/book' + n + '.jpg'" :alt="'Book ' + n"
            class="object-contain w-44 h-60" />
        </div>

        <!-- Extra lege vakken met afgeronde hoeken -->
        <div v-for="n in 10" :key="'empty' + n" class="border bg-gray-200 p-2 rounded-lg h-64">
          <!-- Leeg vak -->
        </div>
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
  </div>
</template>

<script setup>
</script>

<style scoped>
select {
  min-width: 150px;
}

img {
  object-fit: contain; /* Zorgt ervoor dat de afbeelding volledig in het vakje past */
}
</style>
