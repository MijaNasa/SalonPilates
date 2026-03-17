<template>
  <section class="testimonials">
    <div class="container text-center">
      <h2 class="elegant-font">Experiencias Reales</h2>
      <div class="testimonials-slider">
        <div v-for="(t, index) in testimonials" :key="index" class="testimonial-card">
          <div class="stars">★★★★★</div>
          <p class="quote">"{{ t.quote }}"</p>
          <p class="author">{{ t.author }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    quote: 'Excelente lugar, muy buena atención y las profes unas genias total. Súper recomendado.',
    author: 'María Laura'
  },
  {
    quote: 'Desde que empece pilates note un gran cambio en mi postura y dolores de espalda. El ambiente es muy tranquilo.',
    author: 'Julieta S.'
  },
  {
    quote: 'Las clases son muy personalizadas, se nota que saben lo que hacen. Un placer venir cada semana.',
    author: 'Ricardo M.'
  }
];
</script>

<style scoped>
.text-center {
  text-align: center;
}

.testimonials {
  background-color: var(--primary-beige);
}

h2 {
  font-size: 2.5rem;
  color: var(--dark-green);
  margin-bottom: 50px;
}

.testimonials-slider {
  display: flex;
  justify-content: center;
  gap: 30px;
  flex-wrap: wrap;
}

.testimonial-card {
  background-color: var(--white);
  padding: 30px;
  border-radius: 20px;
  max-width: 350px;
  box-shadow: var(--shadow);
  text-align: left;
}

.stars {
  color: #ffc107;
  margin-bottom: 15px;
}

.quote {
  font-style: italic;
  color: var(--text-dark);
  margin-bottom: 20px;
}

.author {
  font-weight: 700;
  color: var(--dark-green);
}
</style>
