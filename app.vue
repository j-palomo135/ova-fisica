<template>
  <div class="app">
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" >
<link href="https://fonts.googleapis.com/css2?family=Bitter:ital,wght@0,100..900;1,100..900&family=Faculty+Glyphic&family=Libre+Bodoni:ital,wght@0,400..700;1,400..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
    <nav class="navbar">
      <div class="nav-brand">En Movimiento</div>
      <div class="nav-links">
        <NuxtLink to="/"  class="nav-link">Inicio</NuxtLink>
        <NuxtLink to="/contenido" class="nav-link">Contenido</NuxtLink>
        <NuxtLink to="/quiz" class="nav-link">Quiz</NuxtLink>
      </div>
    </nav>
    <NuxtPage />
  </div>
  <footer class="footer">
      <div class="footer-content">
        <img 
          class="footer-image" 
          src="https://th.bing.com/th/id/R.0cee4c4e109e44560fe5dcc2b6cf01fb?rik=boK9Vp1Gr6rJ1A&pid=ImgRaw&r=0" 
          alt="Logo del OVA"
        />
        <div class="footer-text">
          <p>
            &copy; 2024 OVA En Movimiento: Explorando el Mundo Físico. Todos los derechos reservados. 
          </p>
          <p>
            Este sitio web fue creado con fines educativos para explicar los fundamentos del desarrollo web. 
            El contenido no puede ser reproducido sin autorización.
          </p>
          <p>
            Creado por:Juan Palomo - ludis Alvares
          </p>
        </div>
      </div>
    </footer>
</template>

<style>
* {
  font-family:  "Bitter";
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.footer {
  background-color: #333;
  color: white;
  padding: 20px;
  margin-top: 20px;
}

.footer-content {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  max-width: 1200px;
  margin: 0 auto;
}

.footer-image {
  width: 80px;
  height: auto;
  margin-right: 20px;
  border-radius: 8px;
}

.footer-text {
  line-height: 1.6;
  text-align: left;
  font-size: 0.9rem;
}

.footer p {
  margin: 5px 0;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #ffffff;
}

.app {
  min-height: 100vh;
}

.navbar {
  background-color: #2c3e50;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 2rem;
}

.nav-brand {
  color: white;
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  display: flex;
  gap: 20px;
}

.nav-link {
  color: white;
  text-decoration: none;
  padding: 5px 10px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.nav-link:hover {
  background-color: #34495e;
}

.router-link-active {
  background-color: #3498db;
}

@media (max-width: 600px) {
  .navbar {
    flex-direction: column;
    gap: 15px;
    text-align: center;
  }
  
  .nav-links {
    flex-direction: column;
  }
}
</style>
