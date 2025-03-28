<template>
  <div class="min-h-screen bg-white text-gray-900">
    <!-- Hero Section -->
    <section class="px-2 md:px-4 py-10">
      <div class="flex items-center ml-64"> <!-- Flexbox container -->
        <!-- Grotere Afbeelding aan de linkerkant -->
        <img src="/public/images/book4.jpg" alt="Book 4" class="w-52 h-80 object-cover mr-6" />

        <!-- Titel en tekst aan de rechterkant van de afbeelding -->
        <div>
          <h1 class="text-3xl md:text-4xl font-bold text-blue-900 text-left pb-6 mt-4">
            Special collection <br>
            <span class="text-2xl md:text-3xl">- Dirk Lauwaert</span>
          </h1>

          <!-- Kleine tekst met dezelfde uitlijning als de titel -->
          <p class="text-sm text-blue-900 italic lato-font"> 
            Klapstuk 87. Internationaal Dansfestival Leuven. 14-30 oktober.
          </p>

          <!-- Toevoegen van de ingekorte Lorem Ipsum tekst met 60 karakters per regel -->
          <p class="text-sm text-blue-900 lato-font mt-4">
            Lorem Ipsum is simply dummy text of the printing and typesetting <br />
            industry. Lorem Ipsum has been the industry's standard dummy text <br />
            ever since the 1500s, when an unknown printer took a galley of type <br />
            and scrambled it to make a type specimen book. It has survived not <br />
            only five centuries, but also the leap into electronic typesetting, <br />
            remaining essentially unchanged. It was popularised in the 1960s with <br />
            the release of Letraset sheets containing Lorem Ipsum passages, and <br />
            more recently with desktop publishing software like Aldus PageMaker <br />
            including versions of Lorem Ipsum.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
  // Voeg de Google Font-links toe
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
</script>

<style scoped>
  /* Playfair Display font voor de titel */
  .playfair-font {
    font-family: 'Playfair Display', serif;
  }

  /* Lato font voor de kleine tekst */
  .lato-font {
    font-family: 'Lato', sans-serif;
  }

  /* Optioneel: een border rondom de afbeelding om het te accentueren */
  img {
    border: 2px solid #ddd;
    border-radius: 8px;
  }
</style>
