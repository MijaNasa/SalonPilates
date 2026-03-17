<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import AboutSection from './components/AboutSection.vue'
import BenefitsSection from './components/BenefitsSection.vue'
import ClassesSection from './components/ClassesSection.vue'
import GallerySection from './components/GallerySection.vue'
import TestimonialsSection from './components/TestimonialsSection.vue'
import ContactSection from './components/ContactSection.vue'
import CtaSection from './components/CtaSection.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="app-wrapper">
    <Navbar />
    <main>
      <Hero />
      <AboutSection />
      <BenefitsSection />
      <ClassesSection />
      <GallerySection />
      <TestimonialsSection />
      <ContactSection />
      <CtaSection />
    </main>
    <Footer />
  </div>
</template>

<style>
@import './style.css';

.app-wrapper {
  overflow-x: hidden;
}

/* Add smooth scroll */
html {
  scroll-behavior: smooth;
}
</style>
