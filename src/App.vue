<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About/GitHub</RouterLink>
      
      <a href="https://www.youtube.com/" target="_blank">Video Presentation 📺</a>

      <a href="https://app.powerbi.com/" target="_blank" class="cta-button">
        Launch App ↗
      </a>
    </nav>
  </header>

  <RouterView />
</template>

<style>
/* 1. RESET THE APP CONTAINER */
#app {
  width: 100%;
  max-width: 100%;
  margin: 0;
  padding: 0;
  display: block;
}

/* 2. GLOBAL PAGE RESETS */
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  background-color: white;
}

/* 3. HEADER - CENTERED NAV */
header {
  width: 100%;
  background-color: #333;
  padding: 1rem 0; /* Vertical padding only */
  display: flex;
  justify-content: center; /* This centers the nav bar horizontally */
  align-items: center;
}

nav {
  display: flex;
  gap: 40px; /* Increased gap for better spacing */
  align-items: center;
}

nav a {
  color: white;
  text-decoration: none;
  font-size: 1.1rem;
}

nav a:hover {
  text-decoration: underline;
}

/* CTA BUTTON */
.cta-button {
  background-color: #42b883;
  padding: 8px 20px;
  border-radius: 4px;
  font-weight: bold;
  color: white !important;
  text-decoration: none !important;
}

.cta-button:hover {
  background-color: #3aa876;
}

/* 4. MAIN CONTENT - CENTERED TEXT */
main {
  max-width: 800px;
  margin: 0 auto;    /* Centers the block */
  padding: 4rem 2rem;
  text-align: center; /* Centers the text inside the block */
}
</style>