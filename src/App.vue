<template>
  <div class="font-sans scroll-smooth">
    <Navbar />

    <main class="mt-20">
      <section id="inicio">
        <Hero />
      </section>

      <section id="sobre-mi" class="bg-gray-50">
        <About />
      </section>

      <section id="proyectos">
        <Projects />
      </section>

      <!-- NUEVA SECCIÓN DE SERVICIOS -->
      <section id="servicios" class="bg-white">
        <Services />
      </section>

      <section id="contacto" class="bg-gray-50">
        <Contact />
      </section>
    </main>

    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/navbar.vue'
import Hero from './components/inicio.vue'
import About from './components/sobremí.vue'
import Projects from './components/proyectos.vue'
import Services from './components/servicios.vue'
import Contact from './components/contacto.vue'
import Footer from './components/footer.vue'
</script>
