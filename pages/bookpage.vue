<template>
  <div class="min-h-screen bg-white text-gray-900">
    <!-- Hero Section -->
    <section class="px-2 md:px-4 py-10">
      <div class="flex items-start ml-64"> <!-- Flexbox container aangepast -->
        <!-- Grotere Afbeelding aan de linkerkant -->
        <img src="/images/book4.jpg" alt="Book 4" class="w-48 h-72 object-cover mr-6" />

        <!-- Titel en tekst aan de rechterkant van de afbeelding -->
        <div class="flex-grow">
          <h1 class="text-3xl md:text-4xl font-bold text-blue-900 text-left pb-6 mt-4">
            Special collection <br>
            <span class="text-2xl md:text-3xl">- Dirk Lauwaert</span>
          </h1>

          <!-- Kleine tekst met dezelfde uitlijning als de titel -->
          <p class="text-sm text-blue-900 italic lato-font"> 
            Klapstuk 87. Internationaal Dansfestival Leuven. 14-30 oktober.
          </p>

          <!-- Dunne lijn onder de tekst -->
          <div class="w-5/6 mt-2 border-b border-gray-300"></div>

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

          <!-- Dunne lijn onder de tekst -->
          <div class="w-5/6 mt-2 border-b border-gray-300"></div>

          <!-- Grid met 4 rijen -->
          <div class="grid grid-rows-4 grid-cols-2 gap-4 mt-6">
            <!-- Eerste rij (labels) -->
            <div class="text-sm font-semibold text-blue-900">
              <p>Author</p>
              <p>Release Date</p>
              <p>Format</p>
              <p>Features</p>
              <p>Language</p>
              <p>ISBN</p>
            </div>

            <!-- Tweede rij (gegevens) -->
            <div class="text-sm text-gray-600 lato-font">
              <p>Adam Silver</p>
              <p>May 20, 2000</p>
              <p>21x5</p>
              <p>/</p>
              <p>English</p>
              <p>252720</p>
            </div>
          </div>

          <!-- Dunne lijn onder de grid -->
          <div class="w-5/6 mt-2 border-b border-gray-300"></div>
        </div>

        <!-- You may also like sectie (nu met afbeeldingen onder elkaar) -->
        <div class="ml-10">
          <p class="text-sm text-blue-900 font-semibold">You may also like</p>

          <!-- Flexbox voor de afbeeldingen in een verticale rij -->
          <div class="flex flex-col space-y-4 mt-2 border-l border-gray-300 pl-4">
            <img src="/images/book5.jpg" alt="Book 5" class="w-24 h-36 object-cover" />
            <img src="/images/book2.jpg" alt="Book 2" class="w-24 h-36 object-cover" />
            <img src="/images/book3.jpg" alt="Book 3" class="w-24 h-36 object-cover" />
            <img src="/images/book4.jpg" alt="Book 4" class="w-24 h-36 object-cover" />
          </div>
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

  /* Styling voor de grid elementen */
  .grid {
    display: grid;
    grid-template-rows: repeat(4, auto); /* Vier rijen */
    grid-template-columns: repeat(2, 1fr); /* Twee kolommen */
    gap: 1rem; /* Ruimte tussen de rijen en kolommen */
  }

  .grid p {
    margin-bottom: 0.5rem;
  }

  /* Flexbox voor de "You may also like" sectie in een verticale richting */
  .flex {
    display: flex;
    gap: 1rem;
  }

  /* Flexbox container voor de afbeeldingen in een verticale rij */
  .flex-col {
    display: flex;
    flex-direction: column; /* Maak de flexbox verticaal */
    gap: 1rem; /* Ruimte tussen de afbeeldingen */
  }

  /* Toevoegen van een verticale lijn voor de afbeeldingen */
  .border-l {
    border-left: 2px solid #ddd; /* Verticale lijn aan de linkerkant van de container */
  }

  .pl-4 {
    padding-left: 1rem; /* Padding aan de linkerkant om ruimte te creëren tussen de lijn en de afbeeldingen */
  }
</style>
