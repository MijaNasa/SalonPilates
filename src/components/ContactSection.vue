<template>
  <section id="contacto" class="contact">
    <div class="container">
      <div class="contact-grid">
        <div class="contact-info">
          <h2 class="elegant-font">Contacto</h2>
          <p class="mb-40">Reservá tu clase y empezá a cuidar tu cuerpo hoy. Estamos para asesorarte.</p>
          
          <div class="info-item">
            <div class="icon-box">📞</div>
            <div>
              <h3>Teléfono</h3>
              <p>+54 341 000 0000</p>
            </div>
          </div>
          
          <div class="info-item">
            <div class="icon-box">💬</div>
            <div>
              <h3>WhatsApp</h3>
              <p>Consultas y reservas</p>
              <a href="https://wa.me/5493410000000" class="btn btn-whatsapp mt-10">Enviar mensaje</a>
            </div>
          </div>
          
          <div class="info-item">
            <div class="icon-box">📍</div>
            <div>
              <h3>Dirección</h3>
              <p>Rosario, Santa Fe, Argentina</p>
            </div>
          </div>
        </div>
        
        <div class="contact-map">
          <div class="map-placeholder">
            <p>Mapa Interactivo</p>
            <span>Rosario, Santa Fe</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}

.contact-info h2 {
  font-size: 2.5rem;
  color: var(--dark-green);
  margin-bottom: 20px;
}

.mb-40 {
  margin-bottom: 40px;
}

.info-item {
  display: flex;
  gap: 20px;
  margin-bottom: 30px;
}

.icon-box {
  width: 50px;
  height: 50px;
  background-color: var(--accent-green);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
}

.info-item h3 {
  font-size: 1.1rem;
  color: var(--dark-green);
  margin-bottom: 5px;
}

.mt-10 {
  margin-top: 10px;
}

.contact-map {
  height: 400px;
  background-color: var(--secondary-beige);
  border-radius: 20px;
  overflow: hidden;
}

.map-placeholder {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: var(--text-muted);
}

.map-placeholder p {
  font-size: 1.2rem;
  font-weight: 600;
}

@media (max-width: 768px) {
  .contact-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}
</style>
