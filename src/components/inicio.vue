<template>
  <section id="inicio" class="inicio">
    <div class="overlay"></div>

    <div class="contenido">
      <h1 class="titulo">Hola, soy <span>Brayan Yañez</span></h1>
      <p class="descripcion">
        Desarrollador web enfocado en crear experiencias digitales modernas,
        funcionales y visualmente atractivas.
      </p>
      <div class="botones">
        <a href="#proyectos" class="btn">Ver proyectos</a>
        <a href="#contacto" class="btn btn-secundario">Contáctame</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Inicio",
};
</script>

<style scoped>
/* ==================== SECCIÓN INICIO ==================== */
.inicio {
  position: relative;
  width: 100%; /* ✅ evita scroll lateral */
  min-height: 100dvh; /* ✅ usa viewport dinámico (corrige en móviles) */
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: url("/portafolio2.jpg") no-repeat center center;
  background-size: cover;
  overflow: hidden;
  color: white;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* Capa semitransparente */
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.45);
  z-index: 1;
}

/* Contenido centrado */
.contenido {
  position: relative;
  z-index: 2;
  width: 90%;
  max-width: 600px;
  padding: 20px;
  box-sizing: border-box;
}

.titulo {
  font-size: 2.4rem;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 20px;
}

.titulo span {
  color: #0078ff;
}

.descripcion {
  font-size: 1.1rem;
  color: #e0e0e0;
  line-height: 1.5;
  margin-bottom: 30px;
}

.botones {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
}

.btn {
  text-decoration: none;
  background: #0078ff;
  color: white;
  padding: 10px 24px;
  border-radius: 8px;
  font-weight: 500;
  transition: all 0.3s ease;
}

.btn:hover {
  background: #005fd1;
  transform: translateY(-2px);
}

.btn-secundario {
  background: transparent;
  color: #ffffff;
  border: 2px solid #ffffff;
}

.btn-secundario:hover {
  background: #ffffff;
  color: #0078ff;
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 1024px) {
  .inicio {
    min-height: 100dvh;
    background-position: center;
    background-attachment: scroll; /* ✅ evita cortes */
  }

  .titulo {
    font-size: 1.9rem;
  }

  .descripcion {
    font-size: 1rem;
  }

  .botones {
    flex-direction: column;
    gap: 12px;
  }
}

/* ✅ evita scroll lateral y espacios extra */
:global(html),
:global(body) {
  width: 100%;
  overflow-x: hidden !important;
  margin: 0;
  padding: 0;
}
</style>
