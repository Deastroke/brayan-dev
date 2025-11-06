<template>
  <section id="servicios" class="servicios">
    <h2 class="titulo-seccion">
      Servicios
      <span class="linea"></span>
    </h2>

    <div class="grid-servicios">
      <div class="card" v-for="(servicio, index) in servicios" :key="index">
        <div class="icono">
          <i :class="servicio.icono"></i>
        </div>
        <h3>{{ servicio.titulo }}</h3>
        <p>{{ servicio.descripcion }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Servicios",
  data() {
    return {
      servicios: [
        {
          titulo: "Página Informativa",
          descripcion:
            "Ideal para negocios que desean mostrar quiénes son, qué ofrecen y cómo contactarlos. Secciones como inicio, servicios, nosotros y contacto.",
          icono: "fas fa-globe",
        },
        {
          titulo: "Tienda en Línea (E-commerce)",
          descripcion:
            "Vende productos o servicios directamente. Incluye carrito, pasarelas de pago y panel de administración.",
          icono: "fas fa-shopping-cart",
        },
        {
          titulo: "Landing Page",
          descripcion:
            "Perfecta para promociones o campañas específicas. Capta clientes o registros de manera rápida y visual.",
          icono: "fas fa-bullhorn",
        },
        {
          titulo: "Portafolio Profesional",
          descripcion:
            "Muestra tus proyectos, habilidades y experiencia. Ideal para freelancers y creativos.",
          icono: "fas fa-user-tie",
        },
        {
          titulo: "Sistema Web Personalizado",
          descripcion:
            "Aplicaciones a medida, como sistemas de control interno, gestión de clientes o inventarios.",
          icono: "fas fa-cogs",
        },
        {
          titulo: "Mantenimiento y Actualización",
          descripcion:
            "Mejoras de rendimiento, seguridad y diseño en sitios ya existentes, manteniendo todo optimizado.",
          icono: "fas fa-tools",
        },
      ],
    };
  },
};
</script>

<style scoped>
.servicios {
  background: #ffffff;
  padding: 80px 20px;
  text-align: center;
}

/* Título con línea azul */
.titulo-seccion {
  font-size: 2rem;
  font-weight: 700;
  color: #222;
  margin-bottom: 50px;
  position: relative;
  display: inline-block;
}

.linea {
  display: block;
  width: 70px;
  height: 3px; /* 🔹 más delgada */
  background-color: #0078ff;
  margin: 10px auto 0 auto;
  border-radius: 2px;
}

/* Cuadrícula */
.grid-servicios {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  justify-items: center;
}

/* Tarjetas */
.card {
  background: #ffffff;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  padding: 30px 22px;
  max-width: 330px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  text-align: center;
}

.card:hover {
  transform: translateY(-6px);
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.12);
}

.icono {
  font-size: 2.4rem;
  color: #0078ff;
  margin-bottom: 15px;
}

.card h3 {
  color: #0078ff;
  font-size: 1.2rem;
  margin-bottom: 12px;
}

.card p {
  color: #555;
  font-size: 0.95rem;
  line-height: 1.6;
}

/* Responsivo */
@media (max-width: 992px) {
  .grid-servicios {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .grid-servicios {
    grid-template-columns: 1fr;
  }

  .card {
    max-width: 100%;
  }
}
</style>
