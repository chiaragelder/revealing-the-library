<template>
  <div>
    <nav class="mb-2">
      <ul class="nav-list flex">
        <li class="nav-item">
          <NuxtLink to="/about">About</NuxtLink>
          <!-- Subnavigatie voor About -->
          <ul class="sub-nav">
            <li><NuxtLink to="/about/practical-information">Practical Information</NuxtLink></li>
            <li><NuxtLink to="/about/us">Us</NuxtLink></li>
          </ul>
        </li>
        <li class="nav-item">
          <NuxtLink to="/books">Books</NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink to="/collections">Collections</NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink to="/loginpage">Login</NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink to="/bookpage">book1</NuxtLink>
        </li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap');

.nav-list {
  display: flex;
  justify-content: flex-start; /* Zorgt dat de lijstitems naar links gaan */
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-item {
  margin-right: 70px; /* Vergroot de ruimte tussen de items */
  position: relative; /* Nodig voor de subnavigatie */
}

.nav-item a {
  text-decoration: none;
  color: #333;
  font-family: 'Playfair Display', serif; /* Zet het lettertype op Playfair Display */
  font-size: 22px; /* Vergroot de tekstgrootte */
  font-weight: 700; /* Maak de tekst vetter */
}

.nav-item a:hover {
  color: #426366;
}

/* Subnavigatie styling */
.sub-nav {
  display: none; /* Verberg de subnavigatie standaard */
  position: absolute;
  top: 100%; /* Zet de subnavigatie direct onder het hoofdnavigatie-item */
  left: 0;
  background-color: #426366; /* Blauwe achtergrond */
  padding: 10px;
  list-style: none;
  margin: 0;
  border-radius: 4px;
  width: auto; /* Laat de breedte automatisch de lengte van de tekst volgen */
  min-width: 160px; /* Stel een minimale breedte in voor consistentie */
}

.sub-nav li {
  padding: 5px 10px;
}

.sub-nav li a {
  color: white; /* Witte tekst in de subnavigatie */
  font-weight: normal; /* Maak de tekst normaal */
}

.sub-nav li a:hover {
  color: #ffdd57; /* Gouden kleur bij hover */
}

/* Toon de subnavigatie bij hover */
.nav-item:hover .sub-nav {
  display: block;
}

/* Zorg ervoor dat de subnavigatie niet over de volgende items komt */
.nav-item:hover .sub-nav {
  z-index: 10;
}
</style>
