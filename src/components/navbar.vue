<template>
  <nav class="navbar">
    <!-- Logo -->
    <div class="logo">
      <img src="/devwork.png" alt="Logo" />
    </div>

    <!-- Enlaces -->
    <ul class="nav-links">
      <li v-for="(link, i) in links" :key="i">
        <a
          :href="link.href"
          :class="{ active: activeLink === link.href }"
          @click="setActive(link.href)"
        >
          {{ link.text }}
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      activeLink: "#inicio", // enlace activo por defecto
      links: [
        { text: "Inicio", href: "#inicio" },
        { text: "Sobre mí", href: "#sobre-mi" },
        { text: "Proyectos", href: "#proyectos" },
        { text: "Contacto", href: "#contacto" },
      ],
    };
  },
  methods: {
    setActive(href) {
      this.activeLink = href;
    },
  },
};
</script>

<style scoped>
/* ==================== NAVBAR ==================== */
.navbar {
  width: 100%;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(12px);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px 0;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
  position: sticky;
  top: 0;
  z-index: 1000;
  transition: background 0.3s ease;
}

/* ==================== LOGO ==================== */
.logo img {
  width: 100px;
  height: auto;
  transition: transform 0.3s ease;
  margin-bottom: 8px;
}

.logo img:hover {
  transform: scale(1.05);
}

/* ==================== ENLACES ==================== */
.nav-links {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 25px;
  margin: 0;
  padding: 0;
  flex-wrap: wrap;
}

.nav-links li a {
  text-decoration: none;
  color: #222;
  font-weight: 500;
  font-size: 1rem;
  padding-bottom: 4px;
  border-bottom: 2px solid transparent;
  transition: color 0.3s ease, border-bottom 0.3s ease;
}

/* Hover */
.nav-links li a:hover {
  color: #0078ff;
  border-bottom: 2px solid #0078ff;
}

/* 🔹 Activo */
.nav-links li a.active {
  color: #0078ff;
  border-bottom: 2px solid #0078ff;
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .navbar {
    padding: 12px 0 18px;
  }

  .logo img {
    width: 100px;
    margin-bottom: 10px;
  }

  .nav-links {
    flex-direction: column;
    gap: 10px;
  }

  .nav-links li a {
    font-size: 1.1rem;
  }
}
</style>
