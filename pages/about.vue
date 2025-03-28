<template>
  <!-- Bovenste sectie -->
  <div class="content-container">
    <div class="flex flex-col items-end pr-8">
      <!-- Titel -->
      <p class="pageTitle playfair-display text-5xl font-semibold text-right" style="color: #353892;">
        About
      </p>

      <!-- Link -->
      <div class="buttonBack font-bold mt-4">
        <NuxtLink to="/books">Access to the collection</NuxtLink>
      </div>
    </div>

    <!-- Afbeelding sectie -->
    <div class="flex justify-center mt-8">
      <img src="/images/image2about.png" alt="About image" class="max-w-full h-auto rounded-lg">
    </div>

    <!-- Subtitel onder de afbeelding, links uitgelijnd -->
    <div class="flex justify-start mt-4 pl-8">
      <p class="subtitle playfair-display text-2xl" style="color: #353892;">
        About Sint-Lukas Library Brussels
      </p>
    </div>

    <!-- Bodytekst onder de subtitel, met Lato font -->
    <div class="flex justify-start mt-6 pl-8">
      <p class="body-text lato-regular text-left leading-relaxed">
        The Sint-Lukas Library Brussels is the specialist library of LUCA School of Arts, located on the Sint-Lukas campus in the vibrant city of Brussels. As part of the KU Leuven library network, our library plays a key role in supporting students, lecturers, and researchers in their artistic and academic development. We provide a rich and diverse collection, tailored services, and a welcoming space designed to foster creativity, study, and collaboration.
      </p>
    </div>

    <!-- Accordion menu -->
    <div class="accordion-container mt-8 pl-8">
      <!-- Practical Information Accordion -->
      <div class="accordion-item">
        <button @click="toggleAccordion('practicalInfo')" class="accordion-header">
          Practical Information
        </button>
        <div v-show="openAccordion.practicalInfo" class="accordion-content">
          <p>LUCA School of ArtsBibliotheek Sint-LukasPaleizenstraat 701030 BRUSSELT +32 2 250 11 33bibliotheek.sintlukas@luca-arts.be
            Maandag tot donderdag van 9 tot 21 u., vrijdag 9 tot 18 u.Monday to Thursday from 9 am to 9 pm, Friday 9 am to 6 pm. You can find us at the library building on the Sint-Lukas campus, located in Schaarbeek, Brussels. The library is easily accessible by public transport and offers extended opening hours to meet the needs of our students, faculty, and researchers.Access to our services is available to all LUCA School of Arts and KU Leuven students and staff.</p>
        </div>
      </div>

      <!-- Our Collections Accordion -->
      <div class="accordion-item">
        <button @click="toggleAccordion('ourCollections')" class="accordion-header">
          Our Collections
        </button>
        <div v-show="openAccordion.ourCollections" class="accordion-content">
          <p>The library houses an extensive and carefully curated collection with a strong focus on visual arts, photography, graphic design, architecture, interior design, film, animation, and comics/graphic novels. In addition to books, we offer access to magazines, e-books, multimedia resources, and image archives. Our collection is continuously expanding, keeping pace with current trends and developments in the creative industries.</p>

          <p>
            The library is home to several special collections, offering unique materials for artistic and academic research:
          </p>
          <ul class="list-disc ml-8">
            <li><strong>Artist’s Books</strong> - Unique and limited-edition books where the book itself is an artwork.</li>
            <li><strong>Rare Books</strong> - Historic and valuable publications on fine arts, architecture, and design.</li>
            <li><strong>Comics & Graphic Novels Collection</strong> - A rich selection with a focus on Belgian and European comic art.</li>
            <li><strong>Photography Collection</strong> - Monographs and theoretical works on influential photographers and contemporary practices.</li>
            <li><strong>Architecture & Design References</strong> - Architectural monographs, urban studies, and material sample books for design inspiration and technical research.</li>
            <li><strong>Archival Material</strong> - Documents and publications preserving the history of Sint-Lukas Brussels.</li>
          </ul>
        </div>
      </div>

      <!-- Workshops & Events Accordion -->
      <div class="accordion-item">
        <button @click="toggleAccordion('workshopsEvents')" class="accordion-header">
          Workshops & Events
        </button>
        <div v-show="openAccordion.workshopsEvents" class="accordion-content">
          <p>Throughout the academic year, we host a variety of workshops, lectures, and information sessions on topics such as research strategies, academic referencing, copyright, and using specialized databases for the arts. The library also regularly showcases exhibitions and events, providing opportunities for students to present their work and engage with the broader artistic community.</p>
        </div>
      </div>
    </div>

    <!-- Footer Section -->
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

<style>
.content-container {
  margin: 0 auto; /* Center the content */
  padding-left: 50px; /* Add padding to the left */
  padding-right: 50px; /* Add padding to the right */
}

.playfair-display {
  font-family: "Playfair Display", serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}

/* Lato font voor body tekst */
.lato-regular {
  font-family: "Lato", sans-serif;
  font-weight: 400;
  font-style: normal;
}



/* Bodytekst stijl met aangepaste font-size */
.body-text {
  color: #333; /* Standaard tekstkleur voor body */
  line-height: 1.8; /* Ruimte tussen de regels */
  font-size: 15px; /* Pas hier de grootte van de tekst aan */
  max-width: 90ch; /* Verhoog de max-width van 75ch naar 90ch of meer */
  word-wrap: break-word; /* Zorgt ervoor dat woorden breken als ze de limiet overschrijden */
  hyphens: auto; /* Dit helpt om woorden netjes af te breken als het nodig is */
}

/* Stijlen voor de accordion content */
.accordion-content {
  padding: 10px;
  background-color: #f9f9f9;
  border-radius: 5px;
  margin-top: 5px;
  font-family: "Lato", sans-serif; /* Voeg Lato font toe voor de tekst binnen de accordeon */
  max-width: 90ch; /* Verhoog de max-width van 75ch naar 90ch of meer */
  word-wrap: break-word; /* Zorgt ervoor dat lange woorden netjes afbreken */
  hyphens: auto; /* Dit helpt bij het netjes afbreken van woorden */
}


/* Stijlen voor de accordion */
.accordion-container {
  width: 100%;
}

.accordion-item {
  margin-bottom: 10px;
}

.accordion-header {
  background-color: transparent; /* Verwijder de blauwe achtergrondkleur */
  color: #333; /* Zet de tekstkleur naar zwart */
  font-family: "Playfair Display", serif; /* Zet de font naar Playfair Display */
  font-size: 18px;
  padding: 10px;
  width: 100%;
  text-align: left;
  cursor: pointer;
  border: 1px solid #ffffff; /* Voeg een lichte rand toe om de knop af te bakenen */
  border-radius: 5px;
  transition: background-color 0.3s;
}

.accordion-header:hover {
  background-color: #f4f4f4; /* Achtergrondkleur als je met de muis over de header beweegt */
}


/* Lijststijl voor de unordered list */
ul {
  list-style-type: disc;
  padding-left: 20px; /* Zorgt voor een nette uitlijning van de lijst */
}

ul li {
  margin-bottom: 5px; /* Ruimte tussen de lijstitems */
}

/* Footer stijlen */
.footer {
  background-color: white; /* Verwijderde grijze achtergrondkleur, nu wit */
}

.footer-line {
  width: fit-content; /* De lijn heeft nu dezelfde breedte als de tekst in de footer */
  margin-bottom: 15px;
  height: 2px;
  background-color: #333; /* Lijnkleur */
}

.footer-text {
  color: #333;
  font-size: 14px;
}
</style>

<script>
export default {
  data() {
    return {
      openAccordion: {
        practicalInfo: false,
        ourCollections: false,
        workshopsEvents: false
      }
    };
  },
  methods: {
    toggleAccordion(section) {
      this.openAccordion[section] = !this.openAccordion[section];
    }
  }
};
</script>
