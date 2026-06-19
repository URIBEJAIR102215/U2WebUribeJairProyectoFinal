# PetPals - Plataforma de Gestión Veterinaria

## Descripción
PetPals es un sitio web personal desarrollado como proyecto académico para la materia de
Fundamentos Web. Simula una plataforma de gestión para un centro veterinario, donde los
dueños de mascotas pueden agendar citas y consultar el historial médico de sus mascotas,
y el personal veterinario puede administrar la agenda diaria y los expedientes de los pacientes.

## Objetivo
Integrar estilos CSS externos, componentes de Bootstrap, diseño mobile-first y
representaciones de datos en formatos JSON y XML dentro de un proyecto web personal.

## Tecnologías utilizadas
- HTML5 semántico
- CSS3 (Flexbox, Grid, media queries, mobile-first)
- Bootstrap 5.3 (Navbar, Carousel, Accordion, Modal, Badges, Tablas responsivas, Botones)
- Font Awesome 6.5 (iconografía)
- JSON y XML (representación de datos simulados)

## Estructura de carpetas
```
PetPals/
│
├── LoginUribe.html
├── RegistroUribe.html
├── VistaUsuario.html
├── VistaVeterinario.html
├── ContactoUribe.html
│
├── css/
│   ├── general.css        (estilos compartidos por todo el sitio)
│   ├── login.css
│   ├── registro.css
│   ├── Usuario.css
│   ├── Veterinario.css
│   └── Contacto.css
│
├── img/
│   └── (imágenes del proyecto: logo, fotos, mapa, etc.)
│
├── data/
│   ├── datos.json
│   └── datos.xml
│
└── README.md
```

## Páginas disponibles
| Página | Archivo | Descripción |
|---|---|---|
| Inicio / Login | `LoginUribe.html` | Carrusel de bienvenida e inicio de sesión |
| Registro | `RegistroUribe.html` | Formulario de registro de nuevos usuarios |
| Panel de Usuario | `VistaUsuario.html` | Mascotas registradas, agenda de citas e historial médico |
| Panel de Veterinario | `VistaVeterinario.html` | Agenda del día, búsqueda de pacientes y expedientes médicos |
| Contacto | `ContactoUribe.html` | Canales de atención, ubicación y preguntas frecuentes |

## Componentes de Bootstrap utilizados
- **Navbar** (con botón hamburguesa `navbar-toggler`) en las 5 páginas
- **Carousel** de bienvenida en la página de inicio
- **Accordion** para las preguntas frecuentes en Contacto
- **Modal** para el detalle de mascota (panel de usuario) y el expediente médico (panel de veterinario)
- **Badges** para representar estados (Confirmada, Pendiente, Urgente, Completado)
- **Tablas responsivas** (`table-responsive`) en las tablas de agenda e historial
- **Botones** (`btn`, `btn-outline-success`, `btn-secondary`) en los paneles

Todos los componentes fueron personalizados con la paleta de colores verde del proyecto
(`#1b5e20`, `#2e7d32`, `#81c784`) para evitar la apariencia genérica predeterminada de Bootstrap.

## Diseño mobile-first
Los estilos en `general.css` y en los archivos CSS específicos están definidos primero para
pantallas pequeñas. Mediante `@media (min-width: ...)` se amplían progresivamente para
tablet (768px) y escritorio (992px). Esto aplica al header, la navegación, la tipografía y
a las cuadrículas (CSS Grid) de tarjetas de contacto, estadísticas y formularios.

## Archivos JSON y XML
Dentro de la carpeta `data/` se incluyen dos archivos que representan la estructura de
los datos simulados que se muestran en los paneles de usuario y veterinario:

- **`datos.json`**: contiene los objetos `mascotas`, `citas` e `historialMedico`.
- **`datos.xml`**: representa la misma información en formato XML, con las etiquetas
  `<mascotas>`, `<citas>` e `<historialMedico>`.

Estos archivos reflejan los mismos datos que actualmente se muestran de forma simulada
directamente en el HTML (tarjetas de mascotas, tabla de agenda y tabla de historial médico).
En una etapa posterior del proyecto, esta información podría obtenerse desde un servidor
o una API conectada a una base de datos real.

### Relación entre la interfaz y los datos (ejemplo: tarjeta de mascota)
| Elemento de la interfaz | Campo JSON / XML |
|---|---|
| Nombre de la mascota | `nombre` |
| Raza | `raza` |
| Edad | `edad` |
| Estado de salud (badge) | `estado` |
| Dueño | `dueño` |
| Fecha de última visita | `ultimaVisita` |

## Instrucciones para ejecutar el proyecto
1. Clonar o descargar el repositorio.
2. Abrir el archivo `LoginUribe.html` directamente en el navegador (no requiere servidor).
3. Navegar entre las páginas usando el menú superior.
4. Para revisar el diseño responsive, usar las herramientas de desarrollador del navegador
   (F12 → modo de diseño adaptable) y probar resoluciones de 375px, 768px y 1366px.

## Autor
Jair Uribe — Universidad de las Fuerzas Armadas ESPE
