<template>
  <section id="beneficios" class="benefits">
    <div class="container text-center">
      <h2 class="elegant-font">Beneficios del Pilates</h2>
      <p class="section-subtitle">Descubrí por qué el Pilates es la clave para una vida más saludable y equilibrada.</p>
      
      <div class="benefits-grid">
        <div v-for="(benefit, index) in benefits" :key="index" class="benefit-card">
          <div class="benefit-icon">{{ benefit.icon }}</div>
          <h3 class="elegant-font">{{ benefit.title }}</h3>
          <p>{{ benefit.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const benefits = [
  {
    title: 'Mejor postura',
    description: 'Alineá tu columna y sentite más alto y cómodo en tu día a día.',
    icon: '🧘'
  },
  {
    title: 'Fortalecimiento muscular',
    description: 'Trabajamos el core y todos los grupos musculares de forma equilibrada.',
    icon: '💪'
  },
  {
    title: 'Mayor flexibilidad',
    description: 'Incrementá tu rango de movimiento y reducí la rigidez muscular.',
    icon: '🌀'
  },
  {
    title: 'Reducción del estrés',
    description: 'Conectá con tu respiración y relajá tu mente mientras te movés.',
    icon: '🌿'
  },
  {
    title: 'Prevención de lesiones',
    description: 'Fortalecé tus articulaciones y mejorá tu equilibrio para evitar caídas y dolores.',
    icon: '🛡️'
  }
];
</script>

<style scoped>
.text-center {
  text-align: center;
}

.benefits {
  background-color: var(--secondary-beige);
}

h2 {
  font-size: 2.5rem;
  color: var(--dark-green);
  margin-bottom: 15px;
}

.section-subtitle {
  color: var(--text-muted);
  max-width: 600px;
  margin: 0 auto 50px;
}

.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 30px;
}

.benefit-card {
  background-color: var(--white);
  padding: 40px 20px;
  border-radius: 20px;
  box-shadow: var(--shadow);
  transition: var(--transition);
}

.benefit-card:hover {
  transform: translateY(-10px);
}

.benefit-icon {
  font-size: 3rem;
  margin-bottom: 20px;
}

.benefit-card h3 {
  font-size: 1.3rem;
  color: var(--dark-green);
  margin-bottom: 15px;
}

.benefit-card p {
  color: var(--text-muted);
  font-size: 0.95rem;
}
</style>
