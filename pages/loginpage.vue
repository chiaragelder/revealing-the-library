<template>
  <div class="w-full h-screen flex">
    <!-- Left Column (Form) -->
    <div class="w-1/2 py-8 pl-16 relative z-8 flex flex-col justify-start items-start bg-white overflow-y-auto">
      <div class="w-full max-w-md">
        <!-- Title and Subtitle -->
        <div class="text-left">
          <h1 class="text-4xl font-semibold text-black">Create an account</h1>
          <p class="text-xl mt-4 text-gray-600 opacity-60">Sint-Lukas Library Brussels</p>
        </div>

        <!-- Input Fields -->
        <div class="mt-6 space-y-4">
          <div>
            <label for="firstName" class="block text-sm font-medium text-gray-900">First name</label>
            <div class="mt-1 border border-gray-300 rounded-md px-3 py-2">
              <input
                type="text"
                name="firstName"
                id="firstName"
                class="w-full text-base text-gray-900 placeholder:text-gray-400 bg-white focus:outline-none appearance-none"
                placeholder="chiara"
              />
            </div>
          </div>

          <div>
            <label for="lastName" class="block text-sm font-medium text-gray-900">Name</label>
            <div class="mt-1 border border-gray-300 rounded-md px-3 py-2">
              <input
                type="text"
                name="lastName"
                id="lastName"
                class="w-full text-base text-gray-900 placeholder:text-gray-400 bg-white focus:outline-none appearance-none"
                placeholder="gelder"
              />
            </div>
          </div>

          <div>
            <label for="email" class="block text-sm font-medium text-gray-900">E-mail</label>
            <div class="mt-1 border border-gray-300 rounded-md px-3 py-2">
              <input
                type="email"
                name="email"
                id="email"
                class="w-full text-base text-gray-900 placeholder:text-gray-400 bg-white focus:outline-none appearance-none"
                placeholder="chiaragelder@gmail.com"
              />
            </div>
          </div>

          <div>
            <label for="password" class="block text-sm font-medium text-gray-900">Password</label>
            <div class="mt-1 border border-gray-300 rounded-md px-3 py-2">
              <input
                type="password"
                name="password"
                id="password"
                class="w-full text-base text-gray-900 placeholder:text-gray-400 bg-white focus:outline-none appearance-none"
                placeholder="*******"
              />
            </div>
          </div>
        </div>

        <!-- Buttons -->
        <div class="mt-6 flex flex-col space-y-3 w-full">
          <button class="w-full bg-black text-white py-2 rounded-md">Create account</button>
          <button class="w-full border border-black text-black py-2 rounded-md">Sign up with Toledo</button>
        </div>
      </div>
    </div>

    <!-- Right Column (Image) -->
    <div class="w-5/6 h-screen relative">
      <img src="/images/image3login.png" alt="Login Image" class="object-cover w-full h-full absolute top-0 left-0">
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

<style>
input:-webkit-autofill {
  box-shadow: 0 0 0px 1000px white inset !important;
  -webkit-text-fill-color: #000 !important;
}
</style>

