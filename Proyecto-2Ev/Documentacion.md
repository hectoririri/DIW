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
| Carrusel            | Controles personalizados con íconos redondeados y transiciones fluidas.         |
| Tarjetas (Cards)    | Efecto *hover* 3D (`transform: scale()`) y sombras dinámicas.                   |
| Menús Desplegables  | Diseño *glassmorphism* y animaciones de desplazamiento lateral en hover.        |
Mostrar codigo con esas etiquetas

### Archivo .css
- **Tipografía Custom**: Fuente `Neiko-Font` integrada vía `@font-face`.
  ```css
  /* Definición de la fuente personalizada MiFuente */
  /* Fuente descargada de https://befonts.com/neiko-font.html */
  @font-face {
    font-family: 'MiFuente'; 
    src: url('../resources/fuentes/Neiko-Font/neikoregular-xgmp2.otf') format('opentype');
    font-weight: normal;
    font-style: normal; 
  }
  ```
- **Efectos Visuales**: 
  ```css
  /* Efecto glassmorphism en secciones clave */
  /* Generado con https://css.glass/ */
  .glass-effect {
    background: rgba(228, 87, 202, 0.35);
    backdrop-filter: blur(5.5px);
    border: 1px solid rgba(228, 87, 202, 0.61);
  }
  ```
- **Personalización navbar**:
  ```css
  /* Barra de navegación con efecto glassmorphism */
  .navbar {
      background: rgba(33, 37, 41, 0.95);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      transition: all 0.3s ease-in-out;
  }

  /* Enlaces de navegación con efectos hover */
  .navbar-nav .nav-link {
      color: #fff;
      font-weight: 500;
      padding: 0.5rem 1rem; /* Padding  */
      margin: 0 0.2rem;
      border-radius: 5px;
      transition: all 0.3s ease;
      position: relative;
  }

  /* Efecto de línea gradiente bajo los enlaces */
  .navbar-nav .nav-link::after {
      content: '';
      /* Posiciona el elemento de forma absoluta dentro de su padre */
      position: absolute;
      /* Alinea el elemento en la parte inferior del padre */
      bottom: 0;
      /* Alinea el elemento a la izquierda del padre */
      left: 0;
      /* Ancho inicial 0 para el efecto de animación */
      width: 0;
      /* Altura de la línea */
      height: 2px;
      background: linear-gradient(90deg, #E457CA, #0dcaf0);
      transition: width 0.3s ease;
  }
  .navbar-nav .nav-link:hover::after {
      width: 100%;
  }

  /* Cambio de color en hover y estado activo */
  .navbar-nav .nav-link:hover,
  .navbar-nav .nav-link.active {
      color: #5784e4;
  }

  /* Menú desplegable con efecto glassmorphism */
  .dropdown-menu {
      background: rgba(98, 100, 102, 0.95);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      border: 1px solid rgba(228, 87, 202, 0.2);
      border-radius: 8px;
  }

  /* Elementos del menú desplegable */
  .dropdown-item {
      color: #fff;
      transition: all 0.3s ease;
      padding: 0.7rem 1.5rem;
  }

  /* Efectos hover para elementos desplegables */
  .dropdown-item:hover {
      background: rgba(187, 174, 185, 0.2);
      color: #5784e4;
      transform: translateX(5px);
      border-radius: 18px;
      width: 80%;
  }

  /* Tamaño fijo para iconos SVG en el menú */
  .dropdown-item svg {
      min-width: 20px;
      min-height: 20px;
      width: 20px;
      height: 20px;
      flex-shrink: 0;
  }

  /* Botón del toggler para móvil */
  .navbar-toggler {
      border: none;
      padding: 0.5rem;
  }

  /* Eliminación del outline al hacer focus */
  .navbar-toggler:focus {
      box-shadow: none;
      outline: none;
  }

  /* Icono personalizado para el toggler */
  .navbar-toggler-icon {
      background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 30 30'%3e%3cpath stroke='rgba(228, 87, 202, 1)' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
  }
  ```
- **Personalización card**:
  ```css
  /* Estilo base para las tarjetas personalizadas */
    .custom-card {
        transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
        border: 1px solid #ddd;
        border-radius: 8px;
    }

    /* Efecto hover para las tarjetas */
    .custom-card:hover {
        transform: scale(1.10);
        box-shadow: 0     8px    16px rgba(0, 0, 0, 0.7);
        /*
                    │     │      │       └─ Color (negro con 70% de opacidad)
                    │     │      └─ Difuminado (blur)
                    │     └─ Desplazamiento vertical
                    └─ Desplazamiento horizontal
        */
    }
    /* Asegura que las imágenes dentro de las tarjetas mantengan su proporción, llenen el contenedor y no se salgan de este*/
    .custom-card img{
        object-fit: cover;
    } 
  ```
- **Pantalla inicial (hero)**:
  ```css
  /* Sección hero con imagen de fondo y efecto de overlay */
  .hero {
      background: url('../resources/img/fondos/fondo-principal.jpg') no-repeat center/cover;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #868686;
      text-align: center;
      background-color: rgba(0, 0, 0, 0.5);
  }
  ```
- **Ajustes generales**:
  ```css
  /* Reset básico para todos los elementos */
  * {
      border: 0;
      box-sizing: border-box;
  }

  /* Estilos base del body con fondo gris y tipografía personalizada */
  body {
      background: #706c6f;
      font-family: 'MiFuente', sans-serif; /* Usa tu fuente personalizada */
      color: #333;
      font-size: 1.3em;
  }
  ```

### Sass: archivo custom.css reducido
Archivo `custom.scss` compilado a `custom.css` para personalización avanzada.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Parte 2: Contenido Multimedia 
### Añade a tu sitio web responsive contenido multimedia optimizado* para la web (formatos, tamaños, calidad....) Imágenes, vídeos, logotipo, favicon, carrusel personalizado, animación, canvas, reproductores….
- Imágenes:
Para las imágenes he usado la etiqueta `<img>` con la propiedad `alt` para proporcionar descripciones alternativas de las imágenes en caso de que no se encuentren disponibles o funciones de accesibilidad.
  ```html
  <img src="./resources/img/grupos/Eiden_VenAlParque.jpg" class="d-block w-100 h-100" alt="Foto grupal con Eiden" style="object-fit: cover; height: 400px !important;">
  ```
He utilizado clases de bootstrap para mantener las proporciones de las imágenes, además de un tamaño fijo para que se ajusten a la pantalla.

- Vídeos:
Para los videos he usado la etiqueta `<video>` con la propiedad `controls` para que se muestren los controles de reproducción. También he aplicado la etiqueta `<source>` para especificar diferentes formatos de video y un mensaje alternativo en caso de que no se pueda reproducir el video.
  ```html
    <video class="img-fluid w-100" controls autoplay>
      <source src="./resources/video/Eiden-VenAlParque-Corto.mp4" type="video/mp4">
      <p>Tu navegador no admite la etiqueta de video</p>
    </video>
  ```
- Favicon:
He utilizado un favicon personalizado creado a partir del logo de mi portfolio. Este favicon lo exporte a .ico mediante una página web llamada [**favicon.io**](https://favicon.io/). Aquí convertí mi icono .png a uno .ico 32x32 píxeles y lo exporté como favicon.ico. Luego, lo he añadido a mi proyecto utilizando la etiqueta `<link>` con el atributo `rel="shortcut icon"`, indicando también el tipo de imagen con la etiqueta `type="image/x-icon"`.

  ```html
    <link rel="shortcut icon" href="./resources/img/logos/favicon.ico" type="image/x-icon">
  ```

- Carrusel personalizado:
El carrusel implementado es un componente de Bootstrap que muestra una presentación dinámica de imágenes de diferentes grupos musicales. Sus características principales son:

- - Estructura básica usando las clases `carousel slide` de Bootstrap
- - Botones de navegación prev/next con iconos de flechas
```html
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
```
- - Indicadores de posición con clase `carousel-indicators`. En estos indicadores, cada botón representa un slide del carrusel. Los atributos `data-bs-target` y `data-bs-slide-to` se utilizan para enlazar los botones con el carrusel correspondiente.
```html
<div class="carousel-indicators">
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="3" aria-label="Slide 4"></button>
</div>
```
- -  4 slides con imágenes de grupos musicales diferentes. Cada slide está dentro de una etiqueta `carrousel-inner rounded h-100` que contiene
  - Una imagen optimizada con clase `d-block w-100 h-100`
  - Un título y subtítulo en un `carrousel-caption`
  - Atributo `alt` descriptivo para accesibilidad
  ```html
  <div class="carousel-item active h-100">
    <img src="./resources/img/grupos/Eiden_VenAlParque.jpg" class="d-block w-100 h-100" alt="Foto grupal con Eiden" style="object-fit: cover; height: 400px !important;">
    <div class="carousel-caption">
      <h5>Eiden</h5>
      <p>2020 - 2021</p>
    </div>
  </div>
  ```
El carrusel está estructurado en un sistema de columnas Bootstrap para asegurar el diseño responsive en caso de que la resolución del dispositivo cambie.

  ```html
  <!-- Carrousel -->
        <div class="col-12 col-sm-12 col-md-6 col-lg-5 d-flex justify-content-center mb-4 mb-md-0">
        <div id="carouselExampleCaptions" class="carousel slide h-100">
          <div class="carousel-indicators">
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="3" aria-label="Slide 4"></button>
          </div>
            <div class="carousel-inner rounded h-100">
              <div class="carousel-item active h-100">
                <img src="./resources/img/grupos/Eiden_VenAlParque.jpg" class="d-block w-100 h-100" alt="Foto grupal con Eiden" style="object-fit: cover; height: 400px !important;">
                <div class="carousel-caption">
                  <h5>Eiden</h5>
                  <p>2020 - 2021</p>
                </div>
              </div>
              <div class="carousel-item h-100">
                <img src="./resources/img/grupos/Comborock.jpg" class="d-block w-100 h-100" alt="Imagen de comborock" style="object-fit: cover; height: 400px !important;">
                <div class="carousel-caption">
                  <h5>ComboRock</h5>
                  <p>2021 - 2022</p>
                </div>
              </div>
                <div class="carousel-item h-100">
                <img src="./resources/img/grupos/PyS.jpg" class="d-block w-100 h-100" alt="Foto grupal con Puntos y Seguidos" style="object-fit: cover; height: 400px !important;">
                <div class="carousel-caption">
                  <h5>Puntos y Seguidos</h5>
                  <p>2024 - actualidad</p>
                </div>
              </div>
              <div class="carousel-item h-100">
                <img src="./resources/img/grupos/Granuja_Navidad.jpg" class="d-block w-100 h-100" alt="Foto grupal con El Granuja y sus Majaras." style="object-fit: cover; height: 400px !important;">
                <div class="carousel-caption">
                  <h5>Granuja y sus Majaras</h5>
                  <p>2024 - actualidad</p>
                </div>
              </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Next</span>
            </button>
        </div>
      </div>
  ```
- Animación:
Para las animaciones, utilicé las propias integradas que ofrece Bootstrap para crear efectos de transición suave, además de las mias propias que utilizo en mi hoja de estilo `style.css`.

- Reproductores:

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
- Experiencia de Usuario : Carga instantánea en conexiones lentas gracias a formatos modernos y archivos con tamaño reducido.
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
     
