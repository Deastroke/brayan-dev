<template>
  <section id="sobre-mi" class="sobre-mi">
    <div class="container">
      <h2 class="titulo">Sobre mí</h2>

      <div class="contenido">
        <p>
          Soy <strong>Brayan Yañes</strong>, Ingeniero en Desarrollo y Gestión de Software,
          egresado de la
          <strong>Universidad Tecnológica de la Zona Metropolitana de Guadalajara (UTZMG)</strong>.
          Me especializo en el desarrollo web con enfoque en la creación de interfaces modernas,
          funcionales y responsivas.
        </p>

        <p>
          Durante mis prácticas profesionales en <strong>Avisa®</strong>,
          trabajé en la <strong>reestructuración completa de la página web</strong> de la empresa,
          implementando un carrusel dinámico, un buscador de servicios funcional y un formulario de contacto
          desarrollado con <strong>HTML, CSS, JavaScript, Node.js y Express</strong>.
          Este proyecto me permitió mejorar mis habilidades en diseño, organización de contenido
          y adaptación a entornos reales.
        </p>

        <p>
          En el <strong>Ayuntamiento de Tlajomulco</strong>, desarrollé un sistema de
          <strong>padrón vehicular</strong> con funcionalidades de registro, edición, eliminación
          y administración de usuarios. Utilicé <strong>Node.js, Express, MongoDB y Laravel</strong>,
          logrando un sistema estable y bien estructurado para la gestión interna.
        </p>

        <p>
          A lo largo de mis estudios y experiencias profesionales he aprendido a trabajar con
          herramientas como <strong>Figma, Lucidchart y Canva</strong>, aplicadas en diseño de interfaces,
          documentación y presentación de proyectos.
        </p>
      </div>

      <!-- HABILIDADES -->
      <div class="habilidades">
        <h3>Habilidades</h3>

        <div class="grid-habilidades">
          <div>
            <h4>Lenguajes</h4>
            <ul>
              <li>HTML5</li>
              <li>CSS3</li>
              <li>JavaScript (ES6+)</li>
              <li>Python</li>
              <li>Node.js</li>
            </ul>
          </div>

          <div>
            <h4>Frameworks y Librerías</h4>
            <ul>
              <li>Express.js</li>
              <li>Vue.js</li>
              <li>React</li>
              <li>Laravel</li>
              <li>Tailwind CSS</li>
              <li>Bootstrap</li>
            </ul>
          </div>

          <div>
            <h4>Bases de Datos</h4>
            <ul>
              <li>MongoDB</li>
              <li>PostgreSQL</li>
              <li>MySQL</li>
            </ul>
          </div>

          <div>
            <h4>Herramientas</h4>
            <ul>
              <li>Figma</li>
              <li>Lucidchart</li>
              <li>Canva</li>
              <li>Visual Studio Code</li>
              <li>Git / GitHub</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SobreMi",
};
</script>

<style scoped>
/* ==================== SECCIÓN SOBRE MÍ ==================== */
.sobre-mi {
  width: 100%;
  background: #ffffff;
  padding: 80px 20px;
  box-sizing: border-box;
  overflow-x: hidden;
}

.container {
  max-width: 1000px;
  width: 100%;
  margin: 0 auto;
}

/* ==================== TÍTULO ==================== */
.titulo {
  text-align: center;
  font-size: 2.2rem;
  font-weight: 700;
  color: #222;
  margin-bottom: 50px;
  position: relative;
}

.titulo::after {
  content: "";
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 3px;
  background: #0078ff;
  border-radius: 3px;
}

/* ==================== TEXTO ==================== */
.contenido {
  display: flex;
  flex-direction: column;
  gap: 25px;
  font-size: 1rem;
  color: #555;
  line-height: 1.8;
  text-align: justify;
  margin-bottom: 60px;
}

.contenido strong {
  color: #0078ff;
}

/* ==================== HABILIDADES ==================== */
.habilidades {
  margin-top: 40px;
}

.habilidades h3 {
  text-align: center;
  font-size: 1.8rem;
  font-weight: 600;
  color: #222;
  margin-bottom: 30px;
}

.grid-habilidades {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 30px;
}

.grid-habilidades h4 {
  color: #0078ff;
  font-size: 1.2rem;
  margin-bottom: 10px;
  font-weight: 600;
  text-align: center;
}

.grid-habilidades ul {
  list-style: none;
  padding: 0;
  text-align: center;
}

.grid-habilidades li {
  color: #444;
  margin-bottom: 8px;
  font-size: 0.95rem;
}

/* ==================== AJUSTE DE IMÁGENES EN MÓVIL ==================== */
@media (max-width: 768px) {
  .sobre-mi {
    padding: 60px 15px;
  }

  .titulo {
    font-size: 1.8rem;
  }

  .contenido {
    font-size: 0.95rem;
  }

  .sobre-mi img {
    width: 220px;
    height: auto;
    display: block;
    margin: 0 auto 25px;
    border-radius: 10px;
  }
}

@media (max-width: 480px) {
  .sobre-mi img {
    width: 180px;
  }
}


/* ==================== SECCIÓN SOBRE MÍ ==================== */
.sobre-mi {
  width: 100%;
  background: #ffffff;
  padding: 80px 20px;
  box-sizing: border-box;
  overflow-x: hidden; /* ✅ Previene scroll lateral */
}

/* Contenedor centrado sin desbordar */
.container {
  max-width: 1000px;
  width: 100%;
  margin: 0 auto;
  box-sizing: border-box;
  overflow-x: hidden; /* ✅ Extra seguridad */
}

/* ==================== GRID HABILIDADES ==================== */
.grid-habilidades {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 30px;
  width: 100%;
  box-sizing: border-box;
  overflow-x: hidden;
}

/* ==================== GLOBAL (opcional si aún aparece scroll) ==================== */
:global(body) {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}

</style>
