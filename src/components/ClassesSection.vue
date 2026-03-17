<template>
  <section id="clases" class="classes">
    <div class="container">
      <div class="header-flex">
        <h2 class="elegant-font">Nuestras Clases</h2>
        <div class="line"></div>
      </div>
      
      <div class="classes-container">
        <div v-for="(cls, index) in classes" :key="index" class="class-item">
          <div class="class-info">
            <h3 class="elegant-font">{{ cls.title }}</h3>
            <p>{{ cls.description }}</p>
          </div>
          <div class="class-tag">{{ cls.tag }}</div>
        </div>
      </div>
      
      <div class="classes-cta">
        <p>¿No sabés cuál es la mejor opción para vos?</p>
        <a href="https://wa.me/5493410000000" class="btn btn-primary">Pedir asesoramiento</a>
      </div>
    </div>
  </section>
</template>

<script setup>
const classes = [
  {
    title: 'Pilates reformer',
    description: 'Clases dinámicas utilizando las camillas reformer para un trabajo integral.',
    tag: 'Popular'
  },
  {
    title: 'Pilates mat',
    description: 'Ejercicios de suelo enfocados en el control y la fuerza abdominal.',
    tag: 'Clásico'
  },
  {
    title: 'Clases grupales',
    description: 'Entrená en equipos reducidos con atención compartida y motivadora.',
    tag: 'Social'
  },
  {
    title: 'Clases personalizadas',
    description: 'Un instructor dedicado exclusivamente a tus objetivos y necesidades.',
    tag: 'Premium'
  },
  {
    title: 'Entrenamiento postural',
    description: 'Enfoque terapéutico para corregir hábitos y aliviar dolores crónicos.',
    tag: 'Salud'
  },
  {
    title: 'Pilates para principiantes',
    description: 'Introducción paso a paso a los principios básicos del método.',
    tag: 'Inicio'
  },
  {
    title: 'Pilates para rehabilitación',
    description: 'Ejercicios adaptados para la recuperación de lesiones bajo supervisión.',
    tag: 'Cuidado'
  },
  {
    title: 'Estiramiento y movilidad',
    description: 'Sesiones enfocadas en ganar amplitud y relajar tensiones profundas.',
    tag: 'Relax'
  }
];
</script>

<style scoped>
.header-flex {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-bottom: 50px;
}

.header-flex h2 {
  font-size: 2.5rem;
  color: var(--dark-green);
  white-space: nowrap;
}

.line {
  height: 2px;
  flex-grow: 1;
  background-color: var(--accent-green);
}

.classes-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

.class-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px;
  background-color: var(--white);
  border: 1px solid var(--primary-beige);
  border-radius: 15px;
  transition: var(--transition);
}

.class-item:hover {
  border-color: var(--accent-green);
  box-shadow: var(--shadow);
}

.class-info h3 {
  font-size: 1.4rem;
  color: var(--text-dark);
  margin-bottom: 10px;
}

.class-info p {
  color: var(--text-muted);
  font-size: 1rem;
}

.class-tag {
  background-color: var(--primary-beige);
  color: var(--dark-green);
  padding: 5px 15px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 700;
  text-transform: uppercase;
}

.classes-cta {
  margin-top: 60px;
  text-align: center;
  padding: 40px;
  background-color: var(--accent-green);
  border-radius: 20px;
  color: var(--dark-green);
}

.classes-cta p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 20px;
}

@media (max-width: 768px) {
  .classes-container {
    grid-template-columns: 1fr;
  }
  .class-item {
    flex-direction: column;
    text-align: center;
    gap: 15px;
  }
}
</style>
