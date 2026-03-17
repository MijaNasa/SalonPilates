<template>
  <section id="galeria" class="gallery">
    <div class="container">
      <h2 class="elegant-font text-center">Nuestra Galería</h2>
      <div class="gallery-grid">
        <div class="gallery-item large">
          <img src="../assets/hero-bg.png" alt="Studio View 1">
          <div class="item-overlay">El Estudio</div>
        </div>
        <div class="gallery-item">
          <img src="../assets/reformer.png" alt="Reformer Close-up">
          <div class="item-overlay">Equipamiento</div>
        </div>
        <div class="gallery-item">
          <img src="../assets/stretching.png" alt="Pilates Mat">
          <div class="item-overlay">Bienestar</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.text-center {
  text-align: center;
}

.gallery {
  padding-bottom: 40px;
}

h2 {
  font-size: 2.5rem;
  color: var(--dark-green);
  margin-bottom: 50px;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 300px);
  gap: 20px;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 15px;
  cursor: pointer;
}

.gallery-item.large {
  grid-row: span 2;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: var(--transition);
}

.gallery-item:hover img {
  transform: scale(1.1);
}

.item-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 20px;
  background: linear-gradient(transparent, rgba(0, 0, 0, 0.7));
  color: var(--white);
  font-weight: 600;
  opacity: 0;
  transition: var(--transition);
}

.gallery-item:hover .item-overlay {
  opacity: 1;
}

@media (max-width: 768px) {
  .gallery-grid {
    grid-template-columns: 1fr;
    grid-template-rows: auto;
  }
  .gallery-item {
    height: 250px;
  }
  .gallery-item.large {
    grid-row: auto;
  }
}
</style>
