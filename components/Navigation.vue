<template>
    <div>
      <nav class="mb-2">
        <ul class="nav-list flex">
          <li class="pr-2">
            <NuxtLink to="/about">About</NuxtLink>
          </li>
          <li class="pr-2">
            <NuxtLink to="/books">Books</NuxtLink>
          </li>
          <li class="pr-2">
            <NuxtLink to="/collections">Collections</NuxtLink>
          </li>
          <li class="pr-2">
            <NuxtLink to="/loginpage">Login</NuxtLink>
          </li>
          <li class="pr-2">
            <NuxtLink to="/bookpage">book1</NuxtLink>
          </li>
        </ul>
      </nav>
    </div>
  </template>
  
  <style scoped>
  
  
  .nav-list {
    display: flex;
    justify-content: flex-start; /* Zorgt dat de lijstitems naar links gaan */
    align-items: center;
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .nav-list li {
    margin-right: 20px;
  }
  
  .nav-list li a {
    text-decoration: none;
    color: #333;
    font-weight: 500;
  }
  
  .nav-list li a:hover {
    color: #007BFF;
  }
  </style>
  