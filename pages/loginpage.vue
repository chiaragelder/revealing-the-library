<template>
  <div class="relative w-full h-screen flex">
    <!-- Inhoud aan de linker kant -->
    <div class="flex-1 p-8 z-10 relative flex flex-col justify-start">
      <!-- Titel en subtitel links uitgelijnd en aan de bovenkant van de pagina -->
      <div class="text-left">
        <h1 class="text-4xl font-semibold text-black">Create an account</h1>
        <p class="text-xl mt-4 text-gray-600 opacity-60">Sint-Lukas Library Brussels</p>
      </div>

      <!-- Invoervelden -->
      <div class="mt-6 grid grid-cols-1 gap-x-6 gap-y-4 sm:grid-cols-6">
        <div class="sm:col-span-4">
          <label for="username" class="block text-sm/6 font-medium text-gray-900">First name</label>
          <div class="mt-1">
            <div class="flex items-center rounded-md bg-white pl-3 border border-gray-200 focus-within:border-indigo-600 max-w-[20em]"> 
              <input
                type="text"
                name="username"
                id="username"
                class="block min-w-0 py-1.5 pr-3 pl-1 text-base text-gray-900 placeholder:text-gray-400 focus:outline-none sm:text-sm/6 w-full"
                placeholder="chiara"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="mt-4 grid grid-cols-1 gap-x-6 gap-y-4 sm:grid-cols-6">
        <div class="sm:col-span-4">
          <label for="username" class="block text-sm/6 font-medium text-gray-900">Name</label>
          <div class="mt-1">
            <div class="flex items-center rounded-md bg-white pl-3 border border-gray-200 focus-within:border-indigo-600 max-w-[20em]"> 
              <input
                type="text"
                name="username"
                id="username"
                class="block min-w-0 py-1.5 pr-3 pl-1 text-base text-gray-900 placeholder:text-gray-400 focus:outline-none sm:text-sm/6 w-full"
                placeholder="gelder"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="mt-4 grid grid-cols-1 gap-x-6 gap-y-4 sm:grid-cols-6">
        <div class="sm:col-span-4">
          <label for="username" class="block text-sm/6 font-medium text-gray-900">E-mail</label>
          <div class="mt-1">
            <div class="flex items-center rounded-md bg-white pl-3 border border-gray-200 focus-within:border-indigo-600 max-w-[20em]"> 
              <input
                type="text"
                name="username"
                id="username"
                class="block min-w-0 py-1.5 pr-3 pl-1 text-base text-gray-900 placeholder:text-gray-400 focus:outline-none sm:text-sm/6 w-full"
                placeholder="chiaragelder@gmail.com"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="mt-4 grid grid-cols-1 gap-x-6 gap-y-4 sm:grid-cols-6">
        <div class="sm:col-span-4">
          <label for="username" class="block text-sm/6 font-medium text-gray-900">Password</label>
          <div class="mt-1">
            <div class="flex items-center rounded-md bg-white pl-3 border border-gray-200 focus-within:border-indigo-600 max-w-[20em]"> 
              <input
                type="password"
                name="password"
                id="password"
                class="block min-w-0 py-1.5 pr-3 pl-1 text-base text-gray-900 placeholder:text-gray-400 focus:outline-none sm:text-sm/6 w-full"
                placeholder="*******"
              />
            </div>
          </div>
        </div>
      </div>

      <!-- Knoppen onder het password veld -->
      <div class="mt-6 flex flex-col space-y-3">
        <button class="w-[20em] bg-black text-white py-2 rounded-md">Create account</button>
        <button class="w-[20em] border border-black text-black py-2 rounded-md">Sign up with Toledo</button>
      </div>
    </div>

    <!-- Afbeelding aan de rechterkant (helft van het scherm) -->
    <div class="right-image-container">
      <img src="/images/image3login.png" alt="Login Image" class="object-cover w-full h-full">
    </div>
  </div>
</template>

<script setup>
// Geen specifieke logica nodig voor deze pagina.
</script>

<style scoped>
img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}

.relative {
  position: relative;
}

.flex {
  display: flex;
  width: 100%;
}

.h-screen {
  height: 100vh;
}

.flex-1 {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding-left: 2rem;
}

.text-left {
  text-align: left;
}

.text-4xl {
  font-size: 2.25rem;
  font-weight: 600;
}

.text-xl {
  font-size: 1.25rem;
}

.mt-4 {
  margin-top: 1rem;
}

.text-gray-800 {
  color: #2d3748;
}

.text-gray-600 {
  color: #718096;
}

input[type="text"] {
  background-color: transparent;
  border: none;
  padding: 10px;
  font-size: 1rem;
  color: #333;
  opacity: 0.6;
}

hr {
  border-color: #D1D1D1;
  border-width: 1px;
  opacity: 0.6;
  margin-top: 0.25rem;
}

.right-image-container {
  width: 60%;
  position: absolute;
  top: 0;
  right: 0;
  z-index: 0;
  padding-right: 0;
}
</style>
