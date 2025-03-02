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
He modificado mi archivo custom.scss añadiendo nuevos colores para Bootstrap, espacios personalizados, medidas de contenedores, personalización de fuente de texto, etc... Mi archivo custom.scss es el siguiente:
```scss
// Colores personalizados
$primary: #1a1a1b;
$secondary: #6c757d;
$success: #28a745;
$info: #17a2b8;
$warning: #ffc107;
$danger: #dc3545;

// Espacios de relleno personalizados
$spacer: 1rem;
$spacers: (
  0: 0,
  1: $spacer * .25,
  2: $spacer * .5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
  6: $spacer * 4
);

// Medidas máximas para los contenedores bootstrap
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px,
  xxl: 1320px
);

// Configuración de fuente personalizada
$font-family-sans-serif: 'Segoe UI', system-ui, -apple-system, sans-serif;
$font-size-base: 1rem;
$line-height-base: 1.6;

// Radio de bordes personalizado
$border-radius: .400rem;
$border-radius-lg: .6rem;
$border-radius-sm: .20rem;
@import "../node_modules/bootstrap/scss/bootstrap";
@import "../node_modules/bootstrap/scss/functions";
@import "../node_modules/bootstrap/scss/variables";
@import "../node_modules/bootstrap/scss/variables-dark";
@import "../node_modules/bootstrap/scss/maps";
@import "../node_modules/bootstrap/scss/mixins";
@import "../node_modules/bootstrap/scss/root";
```
Con el comando  `npm run build` he compilado mi archivo y lo he llamado `reducido.css`. Al compilarlo lo moví a la carpeta `css` y lo he enlazado en mi archivo `index.html` de la siguiente manera:
```html
    <!-- Sin scss <link rel="stylesheet" href="./css/bootstrap.min.css" /> -->
    <!-- Sin scss <link rel="stylesheet" href="./css/style.css"> -->
    <!-- Sin scss <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script> -->
    <!-- Con scss --> <link rel="stylesheet" href="./css/reducido.css"> 
```

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

  - Estructura básica usando las clases `carousel slide` de Bootstrap
  - Botones de navegación prev/next con iconos de flechas
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
  - Indicadores de posición con clase `carousel-indicators`. En estos indicadores, cada botón representa un slide del carrusel. Los atributos `data-bs-target` y `data-bs-slide-to` se utilizan para enlazar los botones con el carrusel correspondiente.
```html
<div class="carousel-indicators">
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
  <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="3" aria-label="Slide 4"></button>
</div>
```
  -  4 slides con imágenes de grupos musicales diferentes. Cada slide está dentro de una etiqueta `carrousel-inner rounded h-100` que contiene
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
  - Animaciones con Bootstrap:
    - Estas son las animaciones que vienen por defecto al crear un modal, carrousel, etc...

  - Animaciones propias `style.css`:
    - Animación hover para agrandar una card:
    ```css
          .custom-card {
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
          }
          .custom-card:hover {
            transform: scale(1.10);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.7);
          }
    ```
    - Animación hover a los items del dropdown menu de la barra de navegación:
    ```css
          .dropdown-item {
            transition: all 0.3s ease;
          }

          .dropdown-item:hover {
              transform: translateX(15px);
              border-radius: 18px;
              width: 80%;
          }
    ```
    - Animación hover a los enlaces de la barra de navegación:
    ```css
      .navbar-nav .nav-link {
          color: #fff;
          font-weight: 500;
          padding: 0.5rem 1rem;
          margin: 0 0.2rem;
          border-radius: 5px;
          transition: all 0.3s ease;
          position: relative;
      }

      .navbar-nav .nav-link::after {
          content: '';
          position: absolute;
          bottom: 0;
          left: 0;
          width: 0;
          height: 2px;
          background: linear-gradient(90deg, #E457CA, #0dcaf0);
          transition: width 0.3s ease;
      }
    ```

### Aplica procesos de optimización a imágenes y vídeos
Para optimizar el tamaño de las imágenes y vídeos, utilicé comprimidores de imágenes y vídeos online, como [**Veed**](https://www.veed.io/es-ES/herramientas/comprimir-video/comprimir-mp4) y [**iloveimg**](https://www.iloveimg.com/es/comprimir-imagen/). Estos comprimidores reducen el tamaño de las imágenes y vídeos sin afectar su calidad.

Por ejemplo, la imagen de la portada, que originalmente pesaba 1.5 MB, fue comprimida a 1.1 MB, reduciendo su tamaño en un 27%. Aunque sea 27%, sigue siendo una reducción significativa, ya que el tamaño de la imagen es bastante grande.

El video del concierto ha pasado de 18,4 MB a 8,46 MB, lo que supone una reducción del 54%. La calidad tanto de video como de audio sigue siendo la misma que la original, por lo que no se pierde calidad en el proceso.

![imagen](https://github.com/user-attachments/assets/1ccbee40-26f0-4bb8-92df-bddaa0f25205)

### Justifica el uso de los diferentes formatos usados
Para el video, he usado el formato mp4, ya que es el formato más utilizado en la web. Además, es compatible con la mayoría de los navegadores y es un formato que ofrece una buena calidad de video y audio. Además, es un formato que se puede comprimir sin perder calidad. Así he podido aprovechar para reducir el tamaño del video al ver que ocupaba bastante.

Para las fotos he usado el formato **jpg, png, y svg**.
- **jpg:** He usado este formato ya que es un formato para imágenes con 24 bits de profundidad de color. Esto me ha permitido sacar más provecho de los colores y detalles de las imágenes con más luces, ya que el formato jpg es capaz de almacenar una gran cantidad de información. También permite comprimir imágenes sin perder calidad, lo que me ha permitido reducir el tamaño estas.
- **png:** He usado este formato para imágenes con menos colores y detalles. Además, es un formato que permite imágenes con transparencia, lo que me ha permitido crear imágenes con transparencia como la del logo de HTML y CSS.
- **svg:** He usado este formato mayormente para logos, ya que es un formato vectorial que permite crear imágenes con líneas y formas. Esto permite que al escalar la imagen, no pierda calidad.*web [svgviewer](https://www.svgviewer.dev/) donde he personalizado y usado los svg.*

### Justifica la importancia de optimizar el contenido multimedia
Optimizar el contenido multimedia es importante por varias razones:
- Ahorro de espacio : Al reducir el tamaño de las imágenes y vídeos, se reduce el espacio que ocupan en el servidor, lo que permite tener más espacio para otros archivos.
- Rendimiento : Reducción del 97% en tamaño de imágenes (ej: fondo-principal.jpg pasó de 2.1MB a 61KB).
- Experiencia de Usuario : Carga instantánea en conexiones lentas gracias a formatos modernos y archivos con tamaño reducido.
- SEO : Mejora en métricas [Core Web Vitals](https://web.dev/articles/vitals) (LCP < 2.5s, CLS < 0.1).

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
Sobre mi web, comprobaré los desafios que pueda aplicar ya que hay ciertos que no puedo por no tener documentación en mi web para ello o se me hace imposible. Por ejemplo, el desafío 2 requiere de poner subtítulos en tu video, y el mio solo es sonido de un concierto de música.
- Desafío 1: Contraste de colores
He comprobado los dos colores de texto y fondo que más utilizo en mi web para demostrar que paso la prueba. En la página [webaim.org](https://webaim.org/resources/contrastchecker/) podemos comprobar si nuestros colores pasan la prueba:
1![imagen](https://github.com/user-attachments/assets/19847716-30bf-4a75-b98e-8bb6919e08a7)
1![imagen](https://github.com/user-attachments/assets/ff2b1005-0bd5-40b1-b571-14d115af16b3)

2![imagen](https://github.com/user-attachments/assets/36c761bf-969a-4ec8-b599-52d3b68ad11c)
2![imagen](https://github.com/user-attachments/assets/3ef1991e-4f72-48da-8324-5daa6a45b4a5)

3![imagen](https://github.com/user-attachments/assets/dbc86ac3-0e32-4e2a-b902-2c61169fa4cd)
3![imagen](https://github.com/user-attachments/assets/f7967823-fca3-4244-94f3-7273875701b0)

- Desafío 4: Idioma
En todos los enlaces de mi proyecto y etiqueta `<html>` he especificado el idioma en el que se encuentra, que en mi caso es `es`. En los enlaces `<a>` y etiqueta `<html>`, con el atributo `lang`, y para indicar la dirección de los enlaces se hace con el atributo `hreflang`:
![imagen](https://github.com/user-attachments/assets/14dee55b-69cd-4f9a-a0ac-303a6574b5af)

- Desafío 5: Texto alternativo en las imágenes
En todas mis etiquetas `<img>` he incluido el atributo `alt` que me permite indicar un texto alternativo para estas imágenes en caso de que no se encuentren disponibles o una persona que lea la página sin verla pueda saber de qué trata la foto:
![imagen](https://github.com/user-attachments/assets/a86a8e15-1f1c-4dc7-8f8c-8fa749fa26d1)

- 

### Realiza sobre tu web los ejercicio planteados en el tema de accesibilidad (apartado 2 actividades 2.2 a 2.6) para la de evaluación, análisis y testeo de accesibilidad web.

### Usa herramientas que te ayuden a determinar si el contenido de tu web cumple con los estándares de accesibilidad.
- Lighthouse : Puntuación de accesibilidad: 92/100.
- WAVE Toolbar : 0 errores críticos detectados.
- Screen Readers : Testeado con NVDA y VoiceOver.

### Analiza la usabilidad de tu web según el apartado 5.2. Análisis de un sitio web bien diseñado
     
