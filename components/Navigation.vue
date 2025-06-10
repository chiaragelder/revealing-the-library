<template>
  <header class="nav-header">
    <div class="logo-container">
      <NuxtLink to="/">
        <img src="assets/styles/AnimatieLOGONieuw.gif" alt="Zoie Logo" class="logo-image" />
      </NuxtLink>
    </div>

    <nav class="nav-bar">
      <ul class="nav-list flex">
        <li class="nav-item"><NuxtLink to="/about">About</NuxtLink></li>
        <li class="nav-item"><NuxtLink to="/collections">Collections</NuxtLink></li>
        <li class="nav-item"><NuxtLink to="/loginpage">Login</NuxtLink></li>
        <li class="nav-item"><NuxtLink to="/books">Books</NuxtLink></li>
        
      </ul>
    </nav>
  </header>
</template>



<style scoped>
.nav-header {
  width: 100%;
  background: white;
  padding: 20px 40px -20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-right: 500px;
  gap: 60px;
  border-bottom: 1px solid #ccc; 
}


.nav-inner {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 1200px;
  width: 100%;
}

/* logo links */
.logo-container {
  flex-shrink: 0;
}

.logo-image {
  height: 150px;
  width: auto;
  min-width: 100px;
  flex-shrink: 0;
  display: block;
  margin-top: -20px;
}

/* nav-bar rechts van logo */
.nav-bar {
  display: flex;
  align-items: center;
}

.nav-list {
  display: flex;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-item {
  margin-right: 30px;
  position: relative;
}

.nav-item:last-child {
  margin-right: 0;
}

.nav-item a {
  text-decoration: none;
  color: #333;
  font-family: 'lato', serif;
  font-size: 17px;
  font-weight: 400;
}

.nav-item a:hover {
  color: #426366;
}

.sub-nav {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #426366;
  padding: 10px;
  list-style: none;
  margin: 0;
  border-radius: 4px;
  min-width: 160px;
}

.sub-nav li {
  padding: 5px 10px;
}

.sub-nav li a {
  color: white;
  font-weight: normal;
}

.sub-nav li a:hover {
  color: #ffdd57;
}

.nav-item:hover .sub-nav {
  display: block;
  z-index: 10;
}


</style>
