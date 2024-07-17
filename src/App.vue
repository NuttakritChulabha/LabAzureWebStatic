<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <h1>Lab Azure Static Web Apps Deploy CI/CD</h1>
    <div class="logo-container">
      <img alt="Microsoft Azure logo" class="logo" src="@/assets/Microsoft_Azure.png" />
    </div>
    <div class="by-text">By</div>
    <div class="logo-container">
      <img alt="Fusion logo" class="logo" src="@/assets/fusion.jpg" />
    </div>

    <div class="info">
      <p>Date: 18 Jul 2024</p>
      <p>Company: Fusion Solution Co.,Ltd.</p>
    </div>

    <div class="link-section">
      <p><a href="https://learn.microsoft.com/en-us/azure/static-web-apps/overview" target="_blank" rel="noopener">What is Azure Static Web Apps?</a></p>
    </div>
    <div class="button-container">
      <RouterLink to="/">
        <button>Main</button>
      </RouterLink>
    </div>
    <div class="button-container">
      <RouterLink to="/extra">
        <button>Extra</button>
      </RouterLink>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  text-align: center;
  background-color: #ffffff;
  color: #000000;
  padding: 2rem 1rem;
}

h1 {
  margin-bottom: 2rem;
}

.logo-container {
  margin-bottom: 1rem;
}

.logo {
  max-width: 90%;
  height: auto;
  display: block;
  margin: 0 auto;
}

.by-text {
  margin: 1rem 0;
  font-size: 1.5rem;
  font-weight: bold;
}

.info {
  margin: 1rem 0;
  font-size: 1.2rem;
}

.link-section {
  margin: 1rem 0;
  font-size: 1.2rem;
}

.link-section a {
  color: #1a73e8;
  text-decoration: none;
}

.link-section a:hover {
  text-decoration: underline;
}

.button-container {
  margin-top: 2rem;
}

button {
  padding: 0.5rem 1rem;
  font-size: 1rem;
  background-color: #1a73e8;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #1669c1;
}

.wrapper {
  text-align: center;
}

nav {
  width: 100%;
  font-size: 1rem;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  color: #000000;
  text-decoration: none;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .logo-container {
    margin-bottom: 2rem;
  }

  .logo {
    margin: 0 2rem;
  }

  header .wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  nav {
    text-align: center;
    margin-left: 0;
    font-size: 1rem;
    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
