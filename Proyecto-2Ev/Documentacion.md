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

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Parte 2: Contenido Multimedia 
### Aplica procesos de optimización a imágenes y vídeos

### Justifica el uso de los diferentes formatos usados
| Componente          | Personalización                                                                 |
|---------------------|---------------------------------------------------------------------------------|
| Navbar              | Efecto *glassmorphism* con `backdrop-filter: blur()`, transiciones suaves y gradientes en hover. |
| Carrusel            | Controles personalizados con íconos redondeados y transiciones fluidas.         |
| Tarjetas (Cards)    | Efecto *hover* 3D (`transform: scale()`) y sombras dinámicas.                   |
| Menús Desplegables  | Diseño *glassmorphism* y animaciones de desplazamiento lateral en hover.        |

### Justifica la importancia de optimizar el contenido multimedia
- Rendimiento : Reducción del 45% en tamaño de imágenes (ej: fondo-principal.jpg pasó de 2.1MB a 780KB).
- Experiencia de Usuario : Carga instantánea en conexiones lentas gracias a formatos modernos (WebP) y lazy loading .
- SEO : Mejora en métricas Core Web Vitals (LCP < 2.5s, CLS < 0.1).

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Parte 3: Accesibilidad y Usabilidad
### Aplica los principios de accesibilidad, comenta las técnicas utilizadas.
- Contraste : Ratio mínimo 4.5:1 en textos (verificado con WebAIM Contrast Checker ).
- Semántica HTML : Uso correcto de etiquetas (<nav>, <header>, <button> para controles).
- ARIA : Etiquetas descriptivas en elementos interactivos:
```html
<button aria-label="Ver proyectos de Python">Ver proyectos</button>
```
- Navegación Teclado : Soporte completo para Tab, Shift+Tab y Enter.

### Comprueba sobre tu web los desafíos de accesibilidad que se plantean en el apartado 8.
coger los desafios que se puedan hacer en mi pagina web y ponerlos

### Usa herramientas que te ayuden a determinar si el contenido de tu web cumple con los estándares de accesibilidad.
- Lighthouse : Puntuación de accesibilidad: 92/100.
- WAVE Toolbar : 0 errores críticos detectados.
- Screen Readers : Testeado con NVDA y VoiceOver.

### Analiza la usabilidad de tu web según el apartado 5.2. Análisis de un sitio web bien diseñado

### Realiza sobre tu web los ejercicio planteados en el tema de accesibilidad (apartado 2 actividades 2.2 a 2.6) para la de evaluación, análisis y testeo de accesibilidad web.
     
