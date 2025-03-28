<template>
    <div>
      <p class="pageTitle playfair-display">
        Curating and visualizing a Library
      </p>
  
      <p class="text-xl">
        This example starts from a yearly currated list of books from the library. The dataset is based on the dataset of LIMO and accessible as a JSON file.
      </p>
  
      <div class="buttonBack font-bold">
        <NuxtLink to="/books">Access to the collection</NuxtLink>
      </div>
    </div>
  </template>

  <style>
  .playfair-display {
  font-family: "Playfair Display", serif;
  font-optical-sizing: auto;
  font-weight: 400; /* Vervang "weight" door een getal zoals 400 of 700 */
  font-style: normal;
}

</style>

