<template>
  <section id="contacto" class="contacto">
    <div class="container">
      <h2 class="titulo">Contacto</h2>
      <p class="descripcion">
        Si estás interesado en contratar mis servicios de desarrollo web o deseas una cotización personalizada,
        completa el siguiente formulario y me pondré en contacto contigo lo antes posible.
      </p>

      <form @submit.prevent="enviarFormulario" class="formulario">
        <div class="campo">
          <label for="nombre">Nombre completo</label>
          <input type="text" id="nombre" v-model="form.nombre" required placeholder="Escribe tu nombre" />
        </div>

        <div class="campo">
          <label for="telefono">Número de teléfono</label>
          <input type="tel" id="telefono" v-model="form.telefono" required placeholder="10 dígitos" />
        </div>

        <div class="campo">
          <label for="email">Correo electrónico</label>
          <input type="email" id="email" v-model="form.email" required placeholder="ejemplo@correo.com" />
        </div>

        <div class="campo">
          <label for="servicio">Tipo de servicio</label>
          <select id="servicio" v-model="form.servicio" required>
            <option disabled value="">Selecciona una opción</option>
            <option>Desarrollo de página web</option>
            <option>Diseño de interfaz (UI/UX)</option>
            <option>Mantenimiento o actualización web</option>
            <option>Consultoría o soporte técnico</option>
            <option>Otro</option>
          </select>
        </div>

        <div class="campo">
          <label for="mensaje">Mensaje o detalles de tu solicitud</label>
          <textarea
            id="mensaje"
            v-model="form.mensaje"
            rows="5"
            required
            placeholder="Describe tu proyecto o la cotización que deseas solicitar..."
          ></textarea>
        </div>

        <button type="submit" class="btn-enviar">Enviar mensaje</button>

        <p v-if="enviado" class="mensaje-exito">
          ¡Gracias! Tu mensaje fue enviado correctamente.
        </p>
      </form>
      <div v-if="notificacion" :class="['notificacion', notificacion.tipo]">
  {{ notificacion.mensaje }}
</div>

    </div>
  </section>
</template>

<script>
export default {
  name: "Contacto",
  data() {
    return {
      form: {
        nombre: "",
        telefono: "",
        email: "",
        servicio: "",
        mensaje: "",
      },
      notificacion: null,
    };
  },
  methods: {
    async enviarFormulario() {
      try {
        const respuesta = await fetch(`${import.meta.env.VITE_API_URL}/enviar-correo`, {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify(this.form),
        });

        if (respuesta.ok) {
          this.mostrarNotificacion("✅ ¡Gracias! Tu mensaje fue enviado correctamente.", "exito");
          this.form = { nombre: "", telefono: "", email: "", servicio: "", mensaje: "" };
        } else {
          this.mostrarNotificacion("⚠️ Hubo un problema al enviar el formulario.", "error");
        }
      } catch (error) {
        console.error("Error al enviar el formulario:", error);
        this.mostrarNotificacion("🚫 Error al conectar con el servidor.", "error");
      }
    },

    mostrarNotificacion(mensaje, tipo) {
      this.notificacion = { mensaje, tipo };
      setTimeout(() => (this.notificacion = null), 4000);
    },
  },
};
</script>



<style scoped>
/* ==================== CONTACTO ==================== */
.contacto {
  width: 100%;
  min-height: 100vh;
  background: url('/portafolio.jpg') center/cover no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 80px 20px;
  box-sizing: border-box;
}

.container {
  max-width: 700px;
  width: 100%;
  background: rgba(255, 255, 255, 0.95);
  padding: 50px;
  border-radius: 15px;
  box-shadow: 0 5px 25px rgba(0, 0, 0, 0.08);
}

/* ==================== TÍTULO ==================== */
.titulo {
  text-align: center;
  font-size: 2rem;
  font-weight: 700;
  color: #222;
  margin-bottom: 10px;
}

.descripcion {
  text-align: center;
  color: #555;
  margin-bottom: 40px;
  font-size: 1rem;
  line-height: 1.6;
}

/* ==================== FORMULARIO ==================== */
.formulario {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.campo {
  display: flex;
  flex-direction: column;
}

label {
  font-weight: 600;
  color: #333;
  margin-bottom: 6px;
}

input,
textarea,
select {
  padding: 12px;
  border-radius: 8px;
  border: 1px solid #ccc;
  font-size: 1rem;
  color: #333;
  transition: border 0.3s ease;
}

input:focus,
textarea:focus,
select:focus {
  outline: none;
  border-color: #0078ff;
}

/* ==================== BOTÓN ==================== */
.btn-enviar {
  background: #0078ff;
  color: white;
  border: none;
  padding: 14px;
  border-radius: 10px;
  font-size: 1rem;
  cursor: pointer;
  font-weight: 600;
  transition: background 0.3s ease, transform 0.2s;
}

.btn-enviar:hover {
  background: #005fcc;
  transform: translateY(-2px);
}

/* ==================== MENSAJE DE ÉXITO ==================== */
.mensaje-exito {
  color: #0078ff;
  font-weight: 600;
  text-align: center;
  margin-top: 10px;
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .container {
    padding: 30px;
  }

  .titulo {
    font-size: 1.8rem;
  }

  .descripcion {
    font-size: 0.95rem;
  }
}

.notificacion {
  position: fixed;
  top: 20px;
  right: 20px;
  background: #0078ff;
  color: white;
  padding: 15px 25px;
  border-radius: 8px;
  font-weight: 600;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  opacity: 0;
  animation: aparecer 0.4s forwards;
  z-index: 9999;
}

.notificacion.exito {
  background: linear-gradient(135deg, #00c851, #007e33);
}

.notificacion.error {
  background: linear-gradient(135deg, #ff4444, #cc0000);
}

@keyframes aparecer {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

</style>
