<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-brand">
          <h2 class="elegant-font">Equilibrio</h2>
          <p>Bienestar físico y mental a través del método Pilates.</p>
        </div>
        <div class="footer-links">
          <h3>Navegación</h3>
          <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#nosotros">Nosotros</a></li>
            <li><a href="#beneficios">Beneficios</a></li>
            <li><a href="#clases">Clases</a></li>
          </ul>
        </div>
        <div class="footer-contact">
          <h3>Contacto</h3>
          <p>Rosario, Santa Fe</p>
          <p>+54 341 000 0000</p>
        </div>
        <div class="footer-social">
          <h3>Redes Sociales</h3>
          <div class="social-icons">
            <a href="#">Instagram</a>
            <a href="#">Facebook</a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 Equilibrio Pilates Studio. Todos los derechos reservados.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: var(--primary-beige);
  padding: 80px 0 40px;
  border-top: 1px solid var(--accent-green);
}

.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 40px;
  margin-bottom: 60px;
}

.footer-brand h2 {
  color: var(--dark-green);
  font-size: 2rem;
  margin-bottom: 20px;
}

.footer-brand p {
  color: var(--text-muted);
}

.footer h3 {
  font-size: 1.2rem;
  color: var(--dark-green);
  margin-bottom: 20px;
}

.footer ul li {
  margin-bottom: 10px;
}

.footer ul li a {
  color: var(--text-muted);
}

.footer ul li a:hover {
  color: var(--dark-green);
}

.footer p {
  color: var(--text-muted);
  margin-bottom: 10px;
}

.social-icons {
  display: flex;
  gap: 20px;
}

.social-icons a {
  color: var(--dark-green);
  font-weight: 600;
}

.footer-bottom {
  text-align: center;
  padding-top: 40px;
  border-top: 1px solid rgba(0, 0, 0, 0.05);
}

.footer-bottom p {
  font-size: 0.9rem;
  color: var(--text-muted);
}

@media (max-width: 992px) {
  .footer-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 576px) {
  .footer-grid {
    grid-template-columns: 1fr;
  }
}
</style>
