# System Urbansys

**Plataforma de gestión residencial inteligente** — Una landing page profesional para Urbansys, la solución todo-en-uno que transforma la administración de comunidades residenciales.

## 🌐 Demo en Vivo

[https://kind-glacier-08ce8810f.6.azurestaticapps.net/](https://kind-glacier-08ce8810f.6.azurestaticapps.net/)

## Problemática

La gestión tradicional de comunidades residenciales enfrenta múltiples deficiencias operativas:

- **Registros dispersos**: La información de residentes, propietarios y mascotas se almacena en papel, hojas de cálculo o sistemas inconexos, lo que genera pérdida de datos y duplicidad.
- **Brechas de comunicación**: Los canales informales como grupos de WhatsApp y correos electrónicos fragmentan la comunicación, provocan desinformación y dificultan el seguimiento de solicitudes.
- **Procesos manuales**: La asignación de parqueaderos, reserva de amenities (zonas BBQ, gimnasio, salones de eventos) y la elaboración de censos se realiza sin automatización, consumiendo tiempo valioso de los administradores.
- **Falta de trazabilidad**: No existe un registro histórico confiable de solicitudes, pagos o comunicaciones, lo que erosiona la confianza entre residentes y administración.

## Solución

**System Urbansys** es una plataforma integral que centraliza, automatiza y moderniza cada aspecto de la gestión residencial:

- **Panel de control centralizado** con métricas en tiempo real sobre ocupación, solicitudes activas y eficiencia del sistema.
- **Censo digital de residentes** con seguimiento granular de propietarios, inquilinos y mascotas, más historial completo de propiedad.
- **Hub de parqueaderos** con gestión dinámica de vehículos, permisos para invitados y asignación automatizada de espacios.
- **Sistema de reservas** en tiempo real para zonas comunes (BBQ, gimnasio, salones de eventos) con reglas de pago integradas.
- **Feed comunitario** con notificaciones push para mantenimiento, reportes anuales y comunicaciones oficiales.
- **Reportes inteligentes** con análisis detallados y datos exportables para toma de decisiones informadas.
- **Seguridad de nivel empresarial** con encriptación end-to-end y cumplimiento normativo.

## Tecnología

| Tecnología | Propósito |
|------------|-----------|
| **Vue 3** (Composition API + `<script setup>`) | Framework frontend progresivo |
| **Vite 7** | Bundler y dev server ultrarrápido |
| **TailwindCSS 3** | Framework de estilos utilitario |
| **Pinia 3** | Estado reactivo global |
| **Vue Router 5** | Enrutamiento SPA |
| **Material Symbols** | Sistema de iconografía |
| **ESLint + Oxlint** | Linting y calidad de código |
| **Prettier** | Formateo consistente |
| **Azure Static Web Apps** | Hosting y despliegue continuo |

## Requisitos

- Node.js >= 20.19.0 o >= 22.12.0
- npm >= 10

## Instalación y Uso

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/urbansys-landing.git
cd urbansys-landing

# Instalar dependencias
npm install

# Iniciar servidor de desarrollo (hot-reload)
npm run dev

# Compilar para producción
npm run build

# Vista previa de la build de producción
npm run preview
```

## Linting y Formateo

```bash
# Ejecutar linters con corrección automática
npm run lint

# Formatear código con Prettier
npm run format
```

## Despliegue

El proyecto está desplegado en **Azure Static Web Apps** con integración continua. La configuración de rutas para SPA se define en `staticwebapp.config.json`:

```json
{
  "navigationFallback": {
    "rewrite": "/index.html",
    "exclude": ["/assets/*", "/*.css", "/*.js"]
  }
}
```

## Estructura del Proyecto

```
src/
├── assets/          # Estilos globales (CSS, fuentes)
├── router/          # Configuración de rutas (Vue Router)
├── stores/          # Estado global (Pinia)
├── views/           # Vistas/páginas
├── App.vue          # Componente raíz
└── main.js          # Punto de entrada
```

## Licencia

Todos los derechos reservados &copy; System Urbansys.
