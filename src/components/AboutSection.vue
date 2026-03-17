<template>
  <section id="nosotros" class="about">
    <div class="container about-grid">
      <div class="about-image">
        <img src="../assets/stretching.png" alt="Sobre Nosotros">
      </div>
      <div class="about-content">
        <h2 class="elegant-font">Sobre Nosotros</h2>
        <p>En <strong>Equilibrio Pilates Studio</strong>, nos dedicamos a transformar vidas a través del movimiento consciente. Nuestro espacio está diseñado para ofrecerte un refugio de tranquilidad donde podés reconectar con tu cuerpo y mente.</p>
        <p>Nos enfocamos en el entrenamiento personalizado, la mejora de la postura y la conciencia corporal. Trabajamos con instructores profesionales que te guiarán en cada paso de tu camino hacia el bienestar integral.</p>
        <div class="about-features">
          <div class="feature">
            <span class="feature-icon">✨</span>
            <p>Atención personalizada</p>
          </div>
          <div class="feature">
            <span class="feature-icon">🧘</span>
            <p>Ambiente tranquilo</p>
          </div>
          <div class="feature">
            <span class="feature-icon">🔝</span>
            <p>Mejora postural</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

.about-image img {
  border-radius: 20px;
  box-shadow: var(--shadow);
}

.about-content h2 {
  font-size: 2.5rem;
  color: var(--dark-green);
  margin-bottom: 25px;
}

.about-content p {
  margin-bottom: 20px;
  color: var(--text-muted);
}

.about-features {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  margin-top: 30px;
}

.feature {
  text-align: center;
  padding: 15px;
  background-color: var(--primary-beige);
  border-radius: 15px;
  transition: var(--transition);
}

.feature:hover {
  transform: translateY(-5px);
  background-color: var(--accent-green);
}

.feature-icon {
  font-size: 1.5rem;
  display: block;
  margin-bottom: 10px;
}

.feature p {
  font-size: 0.9rem;
  font-weight: 600;
  margin-bottom: 0;
  color: var(--dark-green);
}

@media (max-width: 768px) {
  .about-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}
</style>
