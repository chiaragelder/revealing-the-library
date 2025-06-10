<template>
  

  -
      <!-- Homepage content -->

      <div class="flex items-stretch mb-11">
        <!-- Linkerkant -->
        <div class="w-1/2 flex justify-center items-start pt-0 pb-0 mb-0">
          <img 
            src="/images/homepage.png" 
            alt="Bibliotheek Sint-Lukas" 
            class="object-contain w-4/5 h-auto rounded-lg block mb-0"
          />
        </div>

        <!-- Rechterkant -->
        <div class="w-1/2 flex pt-24 pl-16 pr-8 pb-0 mb-0 text-gray-800" style="font-family: 'Playfair Display', serif;">
          <div class="w-1/2 flex flex-col items-end pr-8">
            <h1 class="text-7xl font-bold -ml-3 mb-2">Bibliotheek</h1>
            <h2 class="text-7xl font-bold mb-2 whitespace-nowrap">Sint-Lukas</h2>
            <h3 class="text-7xl font-bold ml-28">Brussel</h3>
          </div>
          <div class="w-1/2 leading-relaxed text-[15px]" style="font-family: 'Lato', sans-serif;">
            <p>
              Welcome to the Sint-Lukas Brussels Library — a vibrant center for art, design, and creativity.
              Our library is a meeting place where students, artists, and researchers come together to explore
              an inspiring collection of books, magazines, and visual materials. Discover unique archives,
              engaging exhibitions, and regular events that celebrate the dynamic world of visual culture.
            </p>
          </div>
        </div>
      </div>

      <!-- Afbeelding onderaan -->
      <div class="w-full mt-0">
        <img 
          src="/images/homepage2.png" 
          alt="Visual Culture" 
          class="w-full object-cover block"
        />
      </div>

      <!-- Events sectie -->
      <div class="flex w-full mt-16 mb-24 px-16 justify-center">
        <div class="w-3/4 text-right pr-8 max-w-[400px]" style="font-family: 'Lato', sans-serif;">
          <p class="text-[16px] leading-relaxed mb-8">
            In our library, we organise fun and engaging events all year round. From lectures and workshops to 
            storytelling sessions and film nights — there’s something for everyone to enjoy. 
            Take a look at our calendar and join us!
          </p>

          <button 
            class="bg-gray-300 text-black px-4 py-2 hover:bg-[#3B7F89] transition-colors duration-300"
          >
            More information
          </button>
        </div>

        <div class="w-1/4 flex items-center pb-20" style="font-family: 'Playfair Display', serif;">
          <h2 class="text-5xl font-bold">Events</h2>
        </div>
      </div>

      <!-- Carrousel -->
      <div class="overflow-x-auto mt-12 pb-4">
        <div class="flex items-end space-x-4 px-16 snap-x snap-mandatory">
          <div class="flex-shrink-0 w-56 h-80 snap-center transition-transform duration-300 hover:scale-105 hover:shadow-xl cursor-pointer">
            <img src="public/images/events1.png" alt="Event Poster 1" class="w-full h-full object-cover " />
          </div>
          <div class="flex-shrink-0 w-64 h-96 snap-center transition-transform duration-300 hover:scale-110 hover:shadow-2xl cursor-pointer">
            <img src="public/images/events2.png" alt="Event Poster 2" class="w-full h-full object-cover " />
          </div>
          <div class="flex-shrink-0 w-64 h-96 snap-center transition-transform duration-300 hover:scale-110 hover:shadow-2xl cursor-pointer">
            <img src="public/images/events3.png" alt="Event Poster 3" class="w-full h-full object-cover " />
          </div>
          <div class="flex-shrink-0 w-64 h-96 snap-center transition-transform duration-300 hover:scale-110 hover:shadow-2xl cursor-pointer">
            <img src="public/images/events4.png" alt="Event Poster 4" class="w-full h-full object-cover " />
          </div>
          <div class="flex-shrink-0 w-56 h-80 snap-center transition-transform duration-300 hover:scale-105 hover:shadow-xl cursor-pointer">
            <img src="public/images/events5.png" alt="Event Poster 5" class="w-full h-full object-cover " />
          </div>
        </div>

        <hr class="border-t border-gray-300 w-full mt-24" />
      </div>

              <!-- Highlight en New in the Library sectie -->
        <div class="flex flex-wrap w-full mt-16 mb-16 px-16">
          <!-- Linkerkant: Highlight of the week -->
          <div class="w-full md:w-1/2 pr-8 mb-12 md:mb-0">
            <div class="grid grid-cols-2 gap-4 items-start">
              <!-- Titel linksboven -->
              <h2 class="text-5xl font-regular leading-tight ml-8 " style="font-family: 'Playfair Display', serif;">
                Highlight of<br />the week
              </h2>

              <!-- Highlight 2 rechtsboven -->
              <img src="public/images/highlight2.png" alt="Highlight 2" class="w-full h-80 object-contain rounded-lg -ml-12 -mb-4" />

              <!-- Highlight 1 linksonder -->
              <img src="public/images/highlight1.png" alt="Highlight 1" class="w-full h-48 object-contain rounded-lg -mt-48" />

              <!-- Highlight 3 rechtsonder (full width over beide kolommen) -->
              <img src="public/images/highlight3.png" alt="Highlight 3" class="w-full h-64 object-contain rounded-lg col-span-2" />
            </div>
          </div>

          <!-- Rechterkant: New in the library -->
          <div class="w-full md:w-1/2 pl-8">
    <div class="flex items-center mb-8">
      <h2 class="text-5xl font-regular mr-8 whitespace-nowrap ml-8" style="font-family: 'Playfair Display', serif;">New in <br />the library</h2>
      <img src="public/images/nieuw1.png" alt="New 1" class="h-44 object-contain  flex-shrink-0 " />
    </div>
    <div class="grid grid-cols-2 gap-4">
      <img src="public/images/nieuw2.png" alt="New 2" class="w-full h-44 object-contain " />
      <img src="public/images/nieuw3.png" alt="New 3" class="w-full h-60 object-contain -ml-24" />
    </div>
  </div>
</div>

  

   
  
  
</template>



