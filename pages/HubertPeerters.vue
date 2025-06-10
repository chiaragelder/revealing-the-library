<template>
  <div class="min-h-screen bg-white text-gray-900">
    <!-- Hero Section -->
    <section class="px-12 md:px-28 py-10">
      <h1 class="text-3xl md:text-4xl font-bold text-blue-900 text-right pb-6 mt-4">
        Special collections <br>
      </h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10 mt-6">
        <div class="order-2 md:order-1">
          <p class="text-base md:text-lg leading-relaxed">
            <strong>Hubert Peeters' </strong> collection was one of the first Pop Art collections in the 1960s and gradually grew into one of the most important in Europe.
          </p>
        </div>
        <div class="w-full h-64 flex items-center justify-end order-1 md:order-2">
          <img src="public/images/Hubert.png" alt="Hubert Peeters Collection"
            class="object-contain max-w-full max-h-full" />
        </div>
      </div>
    </section>

    <!-- Filters -->
    <div class="flex flex-wrap justify-center gap-4 md:gap-10 py-6 border-b px-6 md:px-16">
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
    <section class="px-6 md:px-16 py-10">
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <div v-for="(image, index) in bookImages" :key="index"
          class="border bg-gray-200 flex items-center justify-center p-2 rounded-lg h-64">
          <img :src="'/images/' + image" :alt="'Book ' + (index + 1)"
            class="object-contain w-44 h-60" />
        </div>

        <!-- Lege vakjes -->
        <div v-for="n in 10" :key="'empty' + n"
          class="border bg-gray-200 p-2 rounded-lg h-64">
        </div>
      </div>
    </section>

    <!-- Footer -->
    <div class="footer mt-12 pt-4 pb-4 px-6 md:px-16">
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
const bookImages = [
  'christo.jpg',   // je eerste afbeelding
  'book1.jpg',
  'book2.jpg',
  'book3.jpg',
  'book4.jpg',
  'book5.jpg'
]
</script>

<style scoped>
select {
  min-width: 150px;
}
img {
  object-fit: contain;
}
</style>
