<template>
  <div class="content-page">
    <h1>Contenido del Curso</h1>
    <div class="topics-grid">
      <div class="topic-card">
        <h2>Movimiento Rectilíneo</h2>
        <p>Entendiendo el movimiento en línea recta y sus características.</p>
        <div class="topic-image"></div>
      </div>
      
      <div class="topic-card">
        <h2>Velocidad</h2>
        <p>Conceptos de velocidad instantánea y velocidad media.</p>
        <div class="topic-image"></div>
      </div>
      
      <div class="topic-card">
        <h2>Aceleración</h2>
        <p>Cambios en la velocidad y sus aplicaciones.</p>
        <div class="topic-image"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.content-page {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

h1 {
  color: #2c3e50;
  text-align: center;
  margin-bottom: 40px;
}

.topics-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  padding: 20px;
}

.topic-card {
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.topic-card:hover {
  transform: translateY(-5px);
}

.topic-card h2 {
  color: #3498db;
  margin-bottom: 15px;
}

.topic-card p {
  color: #34495e;
  line-height: 1.6;
}

.topic-image {
  height: 150px;
  background-color: #e0e0e0;
  border-radius: 8px;
  margin-top: 15px;
}
</style>
  