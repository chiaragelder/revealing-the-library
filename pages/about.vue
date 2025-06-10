<template>
  <div class="content-container max-w-[1300px] mx-auto px-6">
    <div class="flex flex-col items-end pr-8">
      <p class="pageTitle playfair-display text-4xl font-semibold text-right" style="color: black;">
        About
      </p>
    </div>

    <!-- Accordion menu -->
    <div class="accordion-container mt-8 pl-8">
      <!-- Practical Information -->
      <div class="accordion-item">
        <button @click="toggleAccordion('practicalInfo')" class="accordion-header group flex flex-col text-left">
          <div class="flex items-center space-x-2 border-b-[1px] border-black w-fit pb-1 text-2xl">
            <span class="accordion-number">0.1</span>
            <span>Practical Information</span>
          </div>
        </button>
        <div v-show="openAccordion.practicalInfo" class="accordion-content mt-4">
          <div class="flex flex-col md:flex-row gap-8">
            <!-- Linkerkolom -->
            <div class="flex-1 space-y-2">
              <p>LUCA School of Arts</p>
              <p>Bibliotheek Sint-Lukas</p>
              <p>Paleizenstraat 70</p>
              <p>1030 BRUSSEL</p>
              <p>T +32 2 250 11 33</p>
              <p>
                <a href="mailto:bibliotheek.sintlukas@luca-arts.be" class="text-blue-600 underline">
                  bibliotheek.sintlukas@luca-arts.be
                </a>
              </p>
              <p>Maandag tot donderdag van 9 tot 21 u., vrijdag 9 tot 18 u.</p>
              <p>Monday to Thursday from 9 am to 9 pm, Friday 9 am to 6 pm</p>

              <div class="mt-4 space-y-1">
                <p class="font-semibold">LIMO LUCA online catalogus</p>
                <a href="#" class="text-blue-600 underline">Nieuwe titels!</a><br>
                <a href="#" class="text-blue-600 underline">Collectie Dirk Lauwaert</a><br>
                <a href="#" class="text-blue-600 underline">Netwerk Brusselse bibliotheken</a>
              </div>
            </div>

            <!-- Rechterkolom -->
            <div class="flex-1 space-y-2">
              <p>
                You can find us at the library building on the Sint-Lukas campus, located in
                <span class="italic">Schaerbeek, Brussels</span>. The library is easily accessible by public transport 
                and offers extended opening hours to meet the needs of our students, faculty, and researchers.
              </p>
              <p>
                Access to our services is available to all LUCA School of Arts and KU Leuven students and staff.
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Our Collections -->
      <div class="accordion-item mt-4">
        <button @click="toggleAccordion('ourCollections')" class="accordion-header group flex flex-col text-left">
          <div class="flex items-center space-x-2 border-b-[1px] border-black w-fit pb-1 text-2xl">
            <span class="accordion-number">0.2</span>
            <span>Reserve & renew</span>
          </div>
        </button>
        <div v-show="openAccordion.ourCollections" class="accordion-content">
          <p>The library houses an extensive and carefully curated collection...</p>
        </div>
      </div>

           <!-- Workshops & Events -->
<div class="accordion-item mt-4">
  <button @click="toggleAccordion('workshopsEvents')" class="accordion-header group flex flex-col text-left">
    <div class="flex items-center space-x-2 border-b-[1px] border-black w-fit pb-1 text-2xl">
      <span class="accordion-number">0.3</span>
      <span>Workshops & Events</span>
    </div>
  </button>
  <div v-show="openAccordion.workshopsEvents" class="accordion-content">

    <!-- Intro tekst -->
    <p class="mt-4">
      Throughout the academic year, we host a variety of workshops, lectures, and information sessions on topics such as research strategies, academic referencing, copyright, and using specialized databases for the arts. The library also regularly showcases exhibitions and events, providing opportunities for students to present their work and engage with the broader artistic community.
    </p>

    <!-- Afbeelding en tekst naast elkaar -->
    <div class="flex flex-col md:flex-row gap-8 mt-8">
      <!-- Afbeelding -->
      <div class="flex-shrink-0">
        <img src="public/images/events1.png" alt="About image" class="max-w-[300px] h-auto">
      </div>

      <!-- Tekstblok -->
      <div class="flex-1 text-left space-y-4 max-w-[800px]">
        <p>
          <strong>Dear readers,</strong><br><br>
          The last essay in our triptych on art education after “Poor Artists” and “Let’s talk about Critique” is “Reports from a Classroom” by art critic, writer and former colleague Dirk Lauwaert (1944 - 2013). The original Dutch text “Berichten uit een klas” originally appeared in De Witte Raaf 50 (July - August 1994). “Berichten uit een klas” was included in the collection “Artikels” (Brussels: Gevaert, 1996).<br><br>
          “Reports from a Classroom” - together with 14 other key texts - was published on the occasion of the integration of the Dirk Lauwaert Collection in the Library of Sint-Lukas. Following the writer’s death in 2013, his family loaned his enormous book collection to the school where he taught for many years.<br><br>
          As you know we host our monthly Book Club at a special table, designed by Sophie Nys in close collaboration with the librarians, to present books from the Dirk Lauwaert Collection. A most fitting place and text to close the triptych.<br><br>
          <em>Lauwaert, D., & Asselberghs, H. (2023). Dirk Lauwaert: Selected Writings, 1983-2008. (R. Desmet, B. Meuleman, & P. J. Perquy, Eds.). Leuven University Press.</em>
        </p>
      </div>
   
</div>


        
        </div>

        
      </div>

            <div class="accordion-item mt-4">
        <button @click="toggleAccordion('ourCollections')" class="accordion-header group flex flex-col text-left">
          <div class="flex items-center space-x-2 border-b-[1px] border-black w-fit pb-1 text-2xl">
            <span class="accordion-number">0.2</span>
            <span>Searching for information using UDC</span>
          </div>
        </button>
        <div v-show="openAccordion.ourCollections" class="accordion-content mt-4">
          <p>
            UDC is een letterwoord uit de bibliotheekwereld wat staat voor Universele Decimale Classificatie. Het is een decimaal systeem dat alle publicaties indeelt in tien hoofdklassen, waarbij iedere hoofdklasse kan worden onderverdeeld in maximaal tien subklassen. Die subklassen kunnen op hun beurt ook weer verder onderverdeeld worden in maximaal tien subsubklassen. Hierdoor ontstaat een hiërarchisch systeem dat het mogelijk maakt om grote hoeveelheden publicaties overzichtelijk en systematisch te ordenen binnen een bibliotheekcollectie.
          </p>

          <p class="mt-4">
            De UDC is gebaseerd op de Dewey Decimal Classification (DDC), die in 1876 werd ontworpen door de Amerikaanse bibliothecaris Meville Dewey. De transformatie van DDC naar UDC vond plaats bij het Institut International de Bibliographie, opgericht door Paul Otlet en Henri LaFontaine. In 1907 verscheen hun <em>Manuel du répertoire bibliographique universel</em>. Tussen 1927 en 1931 volgde de tweede, complete internationale uitgave onder de titel <em>Classification décimale universelle</em>, die de basis vormde voor latere edities.
          </p>

          <p class="mt-4">
            Aanpassingen en wijzigingen aan het systeem worden sindsdien geregeld door de Centrale Classificatie Commissie (CCC) van de Fédération Internationale de Documentation (FID) in Den Haag. Dankzij het gebruik van hulpgetallen en interpunctie maakt de UDC het mogelijk om verschillende begrippen uitgebreid te detailleren en logisch met elkaar te verbinden. Dit zorgt ervoor dat bibliotheken wereldwijd hun collecties volgens een uniforme en flexibele structuur kunnen indelen en toegankelijk maken voor gebruikers.
          </p>
          <div class="mt-6">
            <img src="public/images/UDCinfo.png" class="max-w-[600px] h-auto">
          </div>
        </div>
      </div>
      
    </div>

    <!-- Afbeelding sectie -->
    <div class="flex justify-center mt-24">
      <img src="public/images/image2about.png" alt="About image" class="max-w-full h-auto">
    </div>

    <!-- Subtitel onder de afbeelding -->
    <div class="flex justify-start mt-4 pl-8">
      <p class="subtitle playfair-display text-2xl" style="color: black;">
        About Sint-Lukas Library Brussels
      </p>
    </div>

    <!-- Bodytekst onder de subtitel -->
    <div class="flex justify-start mt-6 pl-8">
      <p class="body-text lato-regular text-left leading-relaxed">
        The Sint-Lukas Library Brussels is the specialist library of LUCA School of Arts, located on the Sint-Lukas campus in the vibrant city of Brussels. As part of the KU Leuven library network, our library plays a key role in supporting students, lecturers, and researchers in their artistic and academic development. We provide a rich and diverse collection, tailored services, and a welcoming space designed to foster creativity, study, and collaboration.
      </p>
      <p>

      </p>
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

    <div class="buttonBack font-bold mt-4">
      <NuxtLink to="/books">Access to the collection</NuxtLink>
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
  background-color: transparent;
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
