<template>
  <section class="proyectos">
    <h2>Mis Proyectos</h2>
    <p class="intro">
      A lo largo de mi formación y práctica profesional, he desarrollado distintos proyectos que me han permitido
      aplicar mis conocimientos en desarrollo web, diseño y programación. A continuación, te presento algunos de ellos:
    </p>

    <!-- Proyecto Avisa® -->
    <div class="proyecto">
      <h3>Avisa®</h3><br><br>
      <div class="imagenes-proyecto">
        <img src="/captura.png" alt="Avisa imagen 1" />
        <img src="/captura1.png" alt="Avisa imagen 2" />
      </div>
      <p>
        Durante mi práctica profesional en Avisa®, participé en la <strong>reestructuración completa de su página web</strong>.
        El sitio incluye un <strong>carrusel dinámico</strong>, un <strong>formulario de contacto funcional</strong> y un
        <strong>buscador de servicios</strong> implementado con JavaScript, Node.js y Express.
        También me encargué de la <strong>responsividad</strong> y optimización visual.
      </p>
       <a href="https://avisa.org.mx/index.html" target="_blank" class="enlace-proyecto">
    Ver proyecto
  </a>
    </div>

    <!-- Proyecto Xtreme -->
    <div class="proyecto">
      <h3>Xtreme</h3><br><br>
      <div class="imagenes-proyecto">
        <img src="/captura3.png" alt="Xtreme imagen 1" />
        <img src="/captura2.png" alt="Xtreme imagen 2" />
      </div>
      <p>
        Proyecto personal enfocado en el desarrollo de un sitio moderno para una marca deportiva. Implementé
        <strong>diseños adaptativos</strong> y una estructura limpia con <strong>HTML, CSS y JavaScript</strong>,
        buscando mejorar la experiencia del usuario con animaciones suaves y navegación intuitiva.
      </p>
      <a href="https://xtremefront.onrender.com/cnc.html" target="_blank" class="enlace-proyecto">
    Ver proyecto
  </a>
    </div>

 <!-- Proyecto Tienda en Línea -->
<div class="proyecto">
  <h3>Tienda en Línea</h3><br><br>

  <!-- 🔹 Imágenes superiores -->
  <div class="imagenes-proyecto">
    <img src="/captura4.png" alt="Xtreme imagen 1" />
    <img src="/captura6.png" alt="Xtreme imagen 2" />
  </div>

  <p>
    Desarrollo de una <strong>plataforma de comercio electrónico</strong> completa, que incluye 
    <strong>carrito de compras</strong>, <strong>categorías de productos</strong> y un 
    <strong>panel de administración</strong> donde el usuario administrador puede 
    <strong>agregar, modificar y eliminar</strong> productos o usuarios.
  </p>
  <p>
    El sistema cuenta con integración de <strong>Stripe</strong> para el procesamiento de pagos 
    en línea y manejo de <strong>tallas, colores y detalles personalizados</strong> de los productos. 
    Aunque las funciones de <strong>inicio de sesión</strong> y <strong>registro</strong> aún no están en línea, 
    el desarrollo del sistema está <strong>finalizado</strong> y listo para su despliegue.
  </p>
  <p>
    El <strong>frontend</strong> fue desarrollado con <strong>React</strong>, mientras que el 
    <strong>backend</strong> se implementó con <strong>Node.js</strong> y <strong>MongoDB</strong>.
    Además, el sitio es <strong>totalmente responsivo</strong>, adaptándose perfectamente a computadoras,
    tablets y dispositivos móviles.
  </p>

  <!-- 🔹 Imágenes inferiores -->
  <div class="imagenes-proyecto">
    <img src="/captura7.png" alt="Xtreme imagen 3" />
    <img src="/captura8.png" alt="Xtreme imagen 4" />
  </div>
</div>


    <!-- Proyecto Ayuntamiento -->
    <div class="proyecto">
      <h3>Proyecto del Ayuntamiento de Tlajomulco</h3><br><br>
<p>
  Durante mi estancia en el <strong>Ayuntamiento de Tlajomulco</strong>, desarrollé una 
  <strong>página interna</strong> enfocada en el <strong>registro y control de información vehicular</strong>. 
  El sistema cuenta con una <strong>base de datos PostgreSQL</strong> para el almacenamiento seguro de la información 
  y permite <strong>generar reportes en PDF</strong> de los registros.
</p>
<p>
  Incluye un <strong>panel de administración</strong> con funcionalidades como 
  <strong>inicio de sesión</strong>, <strong>registro de usuarios</strong>, 
  <strong>modificación</strong> y <strong>eliminación</strong> tanto de usuarios como de vehículos, 
  gestionando los permisos según el <strong>rol del usuario</strong>.
</p>

    </div>



<!-- Proyecto Bot de WhatsApp -->
<div class="proyecto">
  <h3>Bot de WhatsApp</h3><br><br>

  <p>
    Este proyecto corresponde al desarrollo de un <strong>bot automatizado para WhatsApp</strong>, 
    complementado con un <strong>panel de control desarrollado en Flutter</strong>. 
    Su enfoque principal no es la atención al cliente, sino la <strong>automatización y optimización 
    de las acciones internas del trabajador</strong>.
  </p>

  <p>
    El sistema permite al personal registrar y gestionar solicitudes de manera automática 
    a través de <strong>mensajes de WhatsApp</strong>, los cuales son procesados por el bot 
    y reflejados en el panel administrativo. Entre sus principales funciones se encuentran 
    la <strong>generación de tickets</strong>, la <strong>facturación en PDF</strong> 
    y la <strong>creación de cotizaciones</strong> tanto para <strong>productos</strong> 
    como para <strong>servicios</strong>.
  </p>

  <p>
    La estructura del sistema se basa en módulos independientes de 
    <strong>servicios</strong> y <strong>productos</strong>, que permiten una gestión ordenada 
    de la información. Utiliza <strong>Node.js</strong> con <strong>Express</strong> en el backend 
    y <strong>PDFKit</strong> para la generación dinámica de documentos, mientras que la base de datos 
    almacena la información de cada operación registrada.
  </p>

  <p>
    Aunque el proyecto se encuentra <strong>totalmente desarrollado y funcional</strong>, 
    aún <strong>no ha sido desplegado</strong>. Representa una solución eficiente para 
    <strong>automatizar tareas administrativas</strong> y llevar un control centralizado 
    de procesos internos mediante la integración entre WhatsApp y Flutter.
  </p>
</div>


  </section>
</template>


<script>
export default {
  name: "Proyectos",
};
</script>


<style scoped>
.proyectos {
  width: 100%;
  padding: 60px 20px;
  text-align: center;
  box-sizing: border-box;
}

.proyectos h2 {
  font-size: 2rem;
  color: #222;
  margin-bottom: 20px;
  font-weight: 700;
}

.intro {
  font-size: 1.1rem;
  color: #444;
  margin-bottom: 50px;
  line-height: 1.6;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

.proyecto {
  max-width: 900px;
  margin: 0 auto 60px;
  text-align: center;
  background: none;
  border: none;
  box-shadow: none;
  padding: 0;
}

.proyecto h3 {
  font-size: 1.5rem;
  color: #0078ff;
  margin-bottom: 8px;
}

.proyecto p {
  font-size: 1rem;
  color: #333;
  line-height: 1.6;
  margin-bottom: 10px;
}

.linea-azul {
  width: 60px;
  height: 3px;
  background-color: #0078ff;
  margin: 0.5rem auto 1.5rem;
  border-radius: 2px;
}

/* === Galería de imágenes === */
.imagenes-proyecto {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  flex-wrap: wrap;
  margin-bottom: 20px;
}

.imagenes-proyecto img {
  width: calc(50% - 10px);
  max-width: 400px;
  height: 250px; /* todas del mismo alto visual */
  object-fit: contain; /* ✅ muestra la imagen completa sin deformarla */
  border-radius: 8px;
  background-color: #fff; /* para rellenar si sobra espacio */
  box-shadow: none;
  transition: transform 0.3s ease;
}

.imagenes-proyecto img:hover {
  transform: scale(1.03);
}

/* === Botón === */
.enlace-proyecto {
  display: inline-block;
  background: linear-gradient(135deg, #0078ff, #00c6ff);
  color: white;
  font-weight: 600;
  text-decoration: none;
  padding: 12px 30px;
  border-radius: 30px;
  font-size: 1rem;
  margin-top: 25px;
  transition: all 0.3s ease;
  box-shadow: 0 4px 10px rgba(0, 120, 255, 0.3);
}

.enlace-proyecto:hover {
  transform: translateY(-3px);
  background: linear-gradient(135deg, #005fcc, #0099ff);
  box-shadow: 0 6px 14px rgba(0, 120, 255, 0.4);
}

/* === Responsivo === */
@media (max-width: 768px) {
  .proyectos {
    padding: 40px 15px;
  }

  .proyectos h2 {
    font-size: 1.6rem;
  }

  .intro {
    font-size: 1rem;
  }

  .proyecto h3 {
    font-size: 1.3rem;
  }

  .proyecto p {
    font-size: 0.95rem;
    text-align: left;
  }

  .imagenes-proyecto img {
    width: 100%;
    height: 200px; /* mismo alto visual en móvil */
    max-width: 100%;
    object-fit: contain; /* ✅ mantiene proporción */
  }
}

html, body {
  overflow-x: hidden;
}
</style>
