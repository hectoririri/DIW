# Proyecto HNG - Portafolio Personal con Bootstrap

![Portada del Proyecto](ruta/a/imagen-portada.jpg) <!-- Añadir ruta real si es necesario -->

## Descripción del Proyecto
Portafolio web moderno y responsivo desarrollado con **HTML, CSS y Bootstrap**, enfocado en mostrar proyectos musicales y de desarrollo. Combina un diseño visual atractivo con funcionalidades interactivas, optimización multimedia y buenas prácticas de accesibilidad.

---

## Parte 1: Web Personalizada

### Web realizada con Bootstrap de temática, contenidos y diseño libres.
Mi página web consiste en un portfolio no tan formal sobre mis dos grandes aficiones; la programación y música. Comento sobre ambos hobbies explicando qué trabajos realizo en cada uno y pruebas de cada uno de estos.
Se pueden ver fotos y videos en formato de carrousel de mis grupos y conciertos en directo. En la parte de la programación, se pueden en ver en formato de cards y carrousel mis diferentes proyectos prácticos que he realizado.

### Rejilla responsive para diferentes dispositivos.
- **Rejilla Bootstrap**: Uso de sistema de columnas (`container`, `row`, `col-*`) para adaptación automática a dispositivos móviles, tablets y desktops.
- **Media Queries Personalizadas**: Ajustes específicos para navegación en móviles (ej: menú hamburguesa con icono SVG personalizado).

### Diferentes componentes de bootstrap.
| Componente          | Personalización                                                                 |
|---------------------|---------------------------------------------------------------------------------|
| Navbar              | Efecto *glassmorphism* con `backdrop-filter: blur()`, transiciones suaves y gradientes en hover. |
| Carrusel            | Controles personalizados con íconos redondeados y transiciones fluidas.         |
| Tarjetas (Cards)    | Efecto *hover* 3D (`transform: scale()`) y sombras dinámicas.                   |
| Menús Desplegables  | Diseño *glassmorphism* y animaciones de desplazamiento lateral en hover.        |

### Archivo .css
- **Tipografía Custom**: Fuente `Neiko-Font` integrada vía `@font-face`.
- **Efectos Visuales**: 
  ```css
  /* Efecto glassmorphism en secciones clave */
  .glass-effect {
    background: rgba(228, 87, 202, 0.35);
    backdrop-filter: blur(5.5px);
    border: 1px solid rgba(228, 87, 202, 0.61);
  }
  ```
- **Personalización navbar**:
- **Personalización card**:
- **Personalización fuente de texto**:
- **Ajustes generales**:

### Sass: archivo custom.css reducido
Archivo `custom.scss` compilado a `custom.css` para personalización avanzada.

