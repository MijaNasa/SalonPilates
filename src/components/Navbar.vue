<template>
  <nav class="navbar" :class="{ 'scrolled': isScrolled }">
    <div class="container nav-container">
      <div class="logo">
        <span class="elegant-font">Equilibrio</span>
      </div>
      <ul class="nav-links" :class="{ 'active': isMobileMenuOpen }">
        <li><a href="#inicio" @click="closeMenu">Inicio</a></li>
        <li><a href="#nosotros" @click="closeMenu">Nosotros</a></li>
        <li><a href="#beneficios" @click="closeMenu">Beneficios</a></li>
        <li><a href="#clases" @click="closeMenu">Clases</a></li>
        <li><a href="#contacto" @click="closeMenu">Contacto</a></li>
      </ul>
      <div class="nav-cta">
        <a href="https://wa.me/5493410000000" class="btn btn-primary">Reservar</a>
      </div>
      <button class="mobile-menu-btn" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

const toggleMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const closeMenu = () => {
  isMobileMenuOpen.value = false;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  padding: 30px 0;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.navbar.scrolled {
  background-color: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(15px);
  padding: 15px 0;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.03);
  border-bottom: 1px solid rgba(255, 255, 255, 0.3);
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.8rem;
  font-weight: 600;
  color: var(--dark-green);
  letter-spacing: -1px;
}

.nav-links {
  display: flex;
  gap: 40px;
}

.nav-links li a {
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--text-dark);
  text-transform: uppercase;
  letter-spacing: 1px;
  position: relative;
  padding: 5px 0;
}

.nav-links li a::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--accent-green);
  transition: width 0.3s ease;
}

.nav-links li a:hover::after {
  width: 100%;
}

.nav-links li a:hover {
  color: var(--dark-green);
}

.btn-primary {
  background-color: var(--accent-green);
  color: var(--dark-green);
  padding: 12px 30px;
  border-radius: 50px;
  font-size: 0.9rem;
  letter-spacing: 1px;
  text-transform: uppercase;
  box-shadow: 0 4px 15px rgba(186, 207, 182, 0.4);
}

.btn-primary:hover {
  background-color: var(--dark-green);
  color: var(--white);
  box-shadow: 0 6px 20px rgba(90, 125, 90, 0.3);
}

.mobile-menu-btn {
  display: none;
  flex-direction: column;
  gap: 6px;
  background: none;
  border: none;
  cursor: pointer;
}

.mobile-menu-btn span {
  display: block;
  width: 25px;
  height: 2px;
  background-color: var(--text-dark);
  transition: var(--transition);
}

@media (max-width: 768px) {
  .navbar {
    padding: 20px 0;
  }
  
  .nav-links {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background-color: var(--white);
    flex-direction: column;
    padding: 40px 20px;
    gap: 25px;
    text-align: center;
    box-shadow: var(--shadow);
    display: none;
    opacity: 0;
    transform: translateY(-10px);
    transition: all 0.3s ease;
  }

  .nav-links.active {
    display: flex;
    opacity: 1;
    transform: translateY(0);
  }

  .mobile-menu-btn {
    display: flex;
  }

  .nav-cta {
    display: none;
  }
}
</style>
