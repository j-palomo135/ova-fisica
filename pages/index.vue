<template>
  <div class="main-container">
    <h1>En Movimiento: Explorando el Mundo Físico</h1>
    <div class="button-container">
      <NuxtLink to="/contenido" class="nav-link">Iniciemos</NuxtLink>
    </div>
    <div class="content-container">
      <h2>Bienvenidos a nuestra OVA de Física</h2>
      <p>En este espacio aprenderemos sobre:</p>
      <ul>
        <li>Conceptos básicos del movimiento</li>
        <li>Velocidad y aceleración</li>
        <li>Aplicaciones en el mundo real</li>
      </ul>
      <div class="video-container">
        <video class="video" controls src="/components/WhatsApp Video 2024-11-18 at 9.06.11 PM.mp4"></video>
      </div>
      <div class="feature-box">
        <h3>¿Qué aprenderás?</h3>
        <p>Descubre los principios fundamentales que rigen el movimiento de los objetos en nuestro universo.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style scoped>
.main-container {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}
/* Contenedor del video */
.video-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

/* Video */
.video {
  width: 80%;
  max-width: 800px;
  border: 2px solid white;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

h1 {
  color: #2c3e50;
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 30px;
}

.button-container {
  display: flex;
  justify-content: center;
  margin: 1rem 0;
}

.nav-link {
  color: white;
  text-decoration: none;
  padding: 10px 20px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
  background-color: #007bff;
  font-size: 1.2em;
  letter-spacing: 3px;
  text-transform: uppercase
}

.nav-link:hover {
  background-color: #0056b3;
}

.content-container {
  background-color: #f8f9fa;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

h2 {
  color: #3498db;
  margin-bottom: 20px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 10px 0;
  border-bottom: 1px solid #e0e0e0;
  color: #34495e;
}

.feature-box {
  background-color: #3498db;
  color: white;
  padding: 20px;
  border-radius: 8px;
  margin-top: 30px;
}

.feature-box h3 {
  margin-top: 0;
}
</style>


  