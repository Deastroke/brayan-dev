<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-logo">
        <img src="/devwork.png" alt="Logo" />
        <span>Brayan Yañez — Desarrollador Web</span>
      </div>

      <ul class="footer-links">
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#sobre-mi">Sobre mí</a></li>
        <li><a href="#proyectos">Proyectos</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </div>

    <div class="footer-bottom">
      <p>© 2025 Mi Portafolio. Todos los derechos reservados.</p>
    </div>

    <!-- Iconos flotantes de redes sociales -->
    <div class="social-floating">
      <a
        href="https://wa.me/5213317593556"
        target="_blank"
        class="bubble whatsapp"
        aria-label="WhatsApp"
      >
        <i class="fab fa-whatsapp"></i>
      </a>

      <a
        href="https://www.facebook.com/brayanramon.yanesvelasco"
        target="_blank"
        class="bubble facebook"
        aria-label="Facebook"
      >
        <i class="fab fa-facebook-f"></i>
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  background: #fff;
  color: #333;
  padding: 30px 20px;
  text-align: center;
  border-top: 2px solid #0078ff;
  position: relative;
}

/* ==================== CONTENIDO PRINCIPAL ==================== */
.footer-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: 10px;
}

.footer-logo img {
  width: 55px;
  height: auto;
  object-fit: contain;
  transition: transform 0.3s ease;
}

.footer-logo img:hover {
  transform: scale(1.05);
}

.footer-logo span {
  font-size: 1rem;
  font-weight: 500;
  color: #333;
}

/* ==================== ENLACES ==================== */
.footer-links {
  list-style: none;
  display: flex;
  gap: 25px;
  padding: 0;
  margin: 0;
}

.footer-links li a {
  color: #555;
  text-decoration: none;
  transition: color 0.3s ease;
  font-size: 0.95rem;
}

.footer-links li a:hover {
  color: #0078ff;
}

/* ==================== COPYRIGHT ==================== */
.footer-bottom {
  margin-top: 20px;
  font-size: 0.9rem;
  color: #666;
  border-top: 1px solid #ddd;
  padding-top: 15px;
}

/* ==================== BURBUJAS FLOTANTES ==================== */
.social-floating {
  position: fixed;
  right: 20px;
  bottom: 25px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  z-index: 1000;
}

.bubble {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 1.5rem;
  text-decoration: none;
  transition: all 0.3s ease;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
}

.whatsapp {
  background-color: #25d366;
}

.facebook {
  background-color: #1877f2;
}

.bubble:hover {
  transform: scale(1.1);
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.3);
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .footer-content {
    gap: 15px;
  }

  .footer-links {
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
  }

  .footer-logo span {
    font-size: 0.9rem;
  }

  .bubble {
    width: 45px;
    height: 45px;
    font-size: 1.2rem;
  }
}
</style>
