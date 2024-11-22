// components/NavBar.vue
<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-logo">
        <h1>En Movimiento: Explorando el Mundo Físico</h1>
      </div>
      <div class="nav-menu">
        <NuxtLink to="/" class="nav-link">Inicio</NuxtLink>
        <NuxtLink to="/contenido" class="nav-link">Contenido</NuxtLink>
        <NuxtLink to="/quiz" class="nav-link">Quiz</NuxtLink>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background: linear-gradient(to right, #2c3e50, #3498db);
  padding: 1rem 0;
  position: sticky;
  top: 0;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  z-index: 1000;
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.nav-logo h1 {
  color: white;
  font-size: 1.5rem;
  font-weight: bold;
  margin: 0;
}

.nav-menu {
  display: flex;
  gap: 2rem;
}

.nav-link {
  color: white;
  text-decoration: none;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  transition: all 0.3s ease;
  font-weight: 500;
}

.nav-link:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}

.nav-link.router-link-active {
  background-color: rgba(255, 255, 255, 0.2);
  border-bottom: 2px solid white;
}

@media (max-width: 768px) {
  .nav-container {
    flex-direction: column;
    gap: 1rem;
    padding: 1rem;
  }

  .nav-logo h1 {
    font-size: 1.2rem;
    text-align: center;
  }

  .nav-menu {
    flex-direction: column;
    width: 100%;
    gap: 0.5rem;
    text-align: center;
  }

  .nav-link {
    display: block;
    padding: 0.8rem;
  }
}
</style>

// app.vue (actualizado)
<template>
  <div class="app">
    <NavBar />
    <main class="main-content">
      <NuxtPage />
    </main>
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  min-height: 100vh;
}

.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main-content {
  flex: 1;
  padding: 2rem;
}

@media (max-width: 768px) {
  .main-content {
    padding: 1rem;
  }
}
</style>
  