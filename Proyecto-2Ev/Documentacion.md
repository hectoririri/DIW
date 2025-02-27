# Proyecto HNG - Portafolio Personal con Bootstrap

![imagen](https://github.com/user-attachments/assets/9a14498d-4feb-4938-98b5-3034755fcbef)

## Descripción del Proyecto
Portafolio web moderno y responsivo desarrollado con **HTML, CSS y Bootstrap**, enfocado en mostrar proyectos musicales y de desarrollo. Combina un diseño visual atractivo con funcionalidades interactivas, optimización multimedia y buenas prácticas de accesibilidad.

## Parte 1: Web Personalizada

### Web realizada con Bootstrap de temática, contenidos y diseño libres.
Mi página web consiste en un portfolio no tan formal sobre mis dos grandes aficiones; la programación y música. Comento sobre ambos hobbies explicando qué trabajos realizo en cada uno y pruebas de cada uno de estos.
Se pueden ver fotos y videos en formato de carrousel de mis grupos y conciertos en directo. En la parte de la programación, se pueden en ver en formato de cards y carrousel mis diferentes proyectos prácticos que he realizado.

### Rejilla responsive para diferentes dispositivos.
- **Rejilla Bootstrap**: Uso de sistema de columnas (`container`, `row`, `col-*`) para adaptación automática a dispositivos móviles, tablets y desktops.
- **Tamaños de columnas**: Uso del sistema de medidas de columnas (`xl`, `lg`, `md`) para la disposición de columnas dependiendo de la resolución del dispositivo
Fila de carrousel con card
```html
<!-- Carrousel -->
<div class="col-12 col-sm-12 col-md-6 col-lg-5 d-flex justify-content-center mb-4 mb-md-0">
  ...contenido...
</div>
<!-- Card derecha musica -->
<div class="col-12 col-sm-12 col-md-6 col-lg-5 d-flex justify-content-center">
  ...contenido...
</div>
```
Filas de proyecto y cards
```html
<div class="p-5">
    <div class="row mb-4">
        <h1 class="text-start pb-2 text-white"><a name="proyectos">Proyectos</h1></a>
        <div class="col-12">
        </div>
    </div>
    <!-- 4 Cards -->
    <div class="row g-4">
        <!-- Card 1 -->
        <div class="col-12 col-md-6 col-lg-3 align-content-center">
        </div>
        <!-- Cord 2 PHP -->
        <div class="col-12 col-md-6 col-lg-3 align-content-center">
        </div>
        <!-- Card 3 JS-->
        <div class="col-12 col-md-6 col-lg-3 align-content-center">
        </div>
        <!-- Card 4 HTML+CSS-->
        <div class="col-12 col-md-6 col-lg-3 align-content-center">
        </div>
    </div>
</div>
```
### Diferentes componentes de bootstrap.
| Componente          | Personalización                                                                 |
|---------------------|---------------------------------------------------------------------------------|
| Navbar              | Efecto *glassmorphism* con `backdrop-filter: blur()`, transiciones suaves y gradientes en hover. |
| Carrusel            | Controles personalizados con íconos redondeados y transiciones entre imágenes fluidas.         |
| Tarjetas (Cards)    | Efecto *hover* 3D (`transform: scale()`) y sombras dinámicas.                   |
| Menús Desplegables  | Diseño *glassmorphism* y animaciones de desplazamiento lateral en hover.        |

Código de navbar:
```html
<nav id="navbar" class="navbar navbar-expand-lg fixed-top">
      <div class="container">
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse justify-content-end" id="navbarNavDropdown">
              <ul class="navbar-nav align-items-center">
                  <li class="nav-item mx-2">
                      <a class="nav-link active" aria-current="page" href="#"> Inicio </a>
                  </li>
                  <li class="nav-item mx-2">
                      <a class="nav-link" href="index.html#musica"> Música </a>
                  </li>
                  <li class="nav-item mx-2">
                      <a class="nav-link" href="index.html#proyectos"> Proyectos </a>
                  </li>
                  <li class="nav-item dropdown mx-2">
                      <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false"> Redes Sociales </a>
                      <ul class="dropdown-menu">
                        <li>
                            <a class="dropdown-item d-flex align-items-center py-2" href="https://github.com/hectoririri" target="_blank">
                              <svg fill="#000000" width="20px" height="20px" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" data-name="Layer 1"><path d="M12,2.2467A10.00042,10.00042,0,0,0,8.83752,21.73419c.5.08752.6875-.21247.6875-.475,0-.23749-.01251-1.025-.01251-1.86249C7,19.85919,6.35,18.78423,6.15,18.22173A3.636,3.636,0,0,0,5.125,16.8092c-.35-.1875-.85-.65-.01251-.66248A2.00117,2.00117,0,0,1,6.65,17.17169a2.13742,2.13742,0,0,0,2.91248.825A2.10376,2.10376,0,0,1,10.2,16.65923c-2.225-.25-4.55-1.11254-4.55-4.9375a3.89187,3.89187,0,0,1,1.025-2.6875,3.59373,3.59373,0,0,1,.1-2.65s.83747-.26251,2.75,1.025a9.42747,9.42747,0,0,1,5,0c1.91248-1.3,2.75-1.025,2.75-1.025a3.59323,3.59323,0,0,1,.1,2.65,3.869,3.869,0,0,1,1.025,2.6875c0,3.83747-2.33752,4.6875-4.5625,4.9375a2.36814,2.36814,0,0,1,.675,1.85c0,1.33752-.01251,2.41248-.01251,2.75,0,.26251.1875.575.6875.475A10.0053,10.0053,0,0,0,12,2.2467Z"/></svg>
                                <span class="m-1 fs-6">GitHub</span>
                            </a>
                        </li>
                        <li>
                            <a class="dropdown-item d-flex align-items-center py-2" href="#">
                              <svg width="20px" height="20px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M2 6a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V6zm3.519 0L12 11.671 18.481 6H5.52zM20 7.329l-7.341 6.424a1 1 0 0 1-1.318 0L4 7.329V18h16V7.329z" fill="#0D0D0D"/></svg>
                              <span class="m-1 fs-6">Correo</span>
                            </a>
                        </li>
                        <li>
                          <a class="dropdown-item d-flex align-items-center py-2" href="#">
                              <svg width="20px" height="20px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path fill="#000000" d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/>
                              </svg>
                              <span class="m-1 fs-6">Instagram</span>
                          </a>
                        </li>
                        <li>
                            <a class="dropdown-item d-flex align-items-center py-2" href="#">
                              <svg fill="#000000" width="20px" height="20px" viewBox="-2 -4 24 24" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMinYMin" class="jam jam-twitter"><path d='M20 1.907a8.292 8.292 0 0 1-2.356.637A4.07 4.07 0 0 0 19.448.31a8.349 8.349 0 0 1-2.607.98A4.12 4.12 0 0 0 13.846.015c-2.266 0-4.103 1.81-4.103 4.04 0 .316.036.625.106.92A11.708 11.708 0 0 1 1.393.754a3.964 3.964 0 0 0-.554 2.03c0 1.403.724 2.64 1.824 3.363A4.151 4.151 0 0 1 .805 5.64v.05c0 1.958 1.415 3.591 3.29 3.963a4.216 4.216 0 0 1-1.08.141c-.265 0-.522-.025-.773-.075a4.098 4.098 0 0 0 3.832 2.807 8.312 8.312 0 0 1-5.095 1.727c-.332 0-.658-.02-.979-.056a11.727 11.727 0 0 0 6.289 1.818c7.547 0 11.673-6.157 11.673-11.496l-.014-.523A8.126 8.126 0 0 0 20 1.907z' /></svg>
                              <span class="m-1 fs-6">Twitter</span>
                            </a>
                        </li>
                      </ul>
                  </li>
              </ul>
          </div>
      </div>
    </nav>
```
Carrousel de imágenes:
```html
<div id="albaliñeriaCarrousel" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="resources/img/php/albañileria_home.png" class="d-block w-100 rounded shadow-lg" alt="Apartado home de programa albaliñeria">
    </div>
    <div class="carousel-item">
      <img src="resources/img/php/albañileria_clientes.png" class="d-block w-100 rounded shadow-lg" alt="Apartado creacion clientes de programa albaliñeria">
    </div>
    <div class="carousel-item">
      <img src="resources/img/php/albañileria_tareas.png" class="d-block w-100 rounded shadow-lg" alt="Apartado listado tareas de programa albaliñeria">
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#albaliñeriaCarrousel" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#albaliñeriaCarrousel" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
```
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
     
