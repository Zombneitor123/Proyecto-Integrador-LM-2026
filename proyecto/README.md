# Proyecto Integrador LM 2026

- **Nombre**: Manuel Alonso Bono Torres
- **Usuario de GitHub**: zombneitor123
- **Tema elegido**: Comida Internacional
- **Por qué lo he elegido**: He elegido este tema porque la gastronomía es una de las mejores formas de conocer diferentes culturas, y me apasiona probar y compartir recetas tradicionales de todo el mundo.

## Palabra del día
META

## Qué he hecho en esta entrega
He creado la estructura de carpetas de mi proyecto, guardando una página web index.html y un documento de datos datos.xml sobre mis platos de comida favoritos. También he incluido una imagen en la carpeta img y he configurado el control de versiones con Git y GitHub.

## UD3 · Estructura HTML

### Palabra del día (22/10/2026)
contexto

### Qué le falta a mi index.html
1. Completar los metadatos del `<head>` (`description`, `keywords` y `author`) y el formato del `<title>` (`Inicio | Comida Internacional`).
2. Organizar el contenido del `<body>` en bloques `<div>` comentados y añadir subtítulos `<h3>` para la jerarquía de títulos.
3. Añadir separadores `<hr>`, una cita con `<blockquote>`, una ficha en `<pre>` y entidades HTML como `&copy;`.

### Mapa del sitio

| Fichero | title | Qué contiene |
| :--- | :--- | :--- |
| `index.html` | Inicio \| Comida Internacional | Portada: presentación del proyecto, introducción a las tradiciones e ingredientes, platos favoritos, enlaces al catálogo y a `contacto.html`, ficha técnica en `<pre>` y cita en `<blockquote>`. |
| `platos.html` | Platos \| Comida Internacional | Catálogo completo con todos los platos de `datos.xml` (`Pizza Margarita`, `Sushi de Salmón` y `Tacos al Pastor`) y tabla comparativa de datos (`<table>`) con tiempos, categorías y precios. |
| `historia.html` | Historia \| Comida Internacional | Orígenes e historia cultural de las tres grandes cocinas del proyecto (Italia, Japón y México), técnicas tradicionales y cita histórica sobre patrimonio culinario. |
| `contacto.html` | Contacto \| Comida Internacional | Formulario de contacto (`<form method="post">`) para enviar recetas o apuntarse a los talleres, horarios de atención en `<pre>` y opiniones de lectores en `<blockquote>`. |

### Validación W3C

| Página | Errores detectados por el validador W3C | Cómo se corrigieron |
| :--- | :--- | :--- |
| `index.html` | 0 errores (ningún error ni advertencia en la validación). | No fue necesario realizar correcciones porque la estructura de bloques, títulos y entidades era válida desde el inicio. |
| `platos.html` | 0 errores (ningún error ni advertencia en la validación). | No necesitó correcciones; los caracteres `<` y `>` dentro del bloque `<pre>` ya estaban escapados con `&lt;` y `&gt;`. |
| `historia.html` | `Error: The width attribute on the hr element is obsolete. Use CSS instead.` | Se eliminó el atributo obsoleto `width="80%"` de la etiqueta `<hr>`, dejándola como `<hr>` limpia (`fix(historia)`). |
| `contacto.html` | 0 errores (ningún error ni advertencia en la validación). | No fue necesario realizar correcciones; el documento validó con 0 errores a la primera. |

### Qué he hecho en esta unidad
En esta unidad he transformado mi página inicial en un sitio web completo de cuatro páginas sobre comida internacional siguiendo un mapa del sitio definido en el `README.md`. He completado la cabecera `<head>` con todos sus metadatos, estructurado el cuerpo de cada documento mediante una jerarquía de títulos sin saltos (`h1`, `h2` y `h3`) y agrupado las secciones en bloques `<div>` comentados con sangría coherente. Además, he incorporado citas con `<blockquote>`, fichas alineadas en `<pre>`, entidades HTML nominales y numéricas, volcado todos los elementos de `datos.xml` en `platos.html` y validado todo el sitio en el validador del W3C hasta lograr 0 errores.

## UD5 · Tablas y formularios

### Palabra del día (05/11/2026)
día

### Propósito de la tabla y del formulario
En la página `platos.html` voy a incluir una tabla comparativa con los platos de nuestra carta internacional (país y tradición culinaria, categoría alimentaria, tiempo de elaboración y precio por ración, más un menú degustación y el total). El formulario de la página `contacto.html` servirá para que los visitantes propongan nuevas recetas tradicionales, se inscriban en los talleres de cocina en directo de los sábados o consulten dudas sobre ingredientes y alérgenos.

### Por qué uso `method="post"` y prueba con `method="get"`
Uso `method="post"` en vez de `get` porque el formulario pide datos personales del usuario (nombre, correo y teléfono) además de un texto largo en `<textarea>`, y con `post` viajan ocultos en el cuerpo de la petición HTTP sin quedarse visibles en la URL del navegador.

Al cambiar el formulario temporalmente a `method="get"` y darle a «Enviar consulta», la URL que salió en la barra del navegador fue:
`http://127.0.0.1:5500/proyecto/contacto.html?nombre=Manuel+Alonso+Bono&correo=manuel%40ejemplo.es&telefono=612345678&cocina_favorita=italiana&motivo=proponer_receta&intereses=vegetariano&mensaje=Hola+quiero+mandar+la+receta+de+la+lasana+casera.&enviar=Enviar+consulta`

### Validación W3C (UD5)

| Página | Errores detectados por el validador W3C | Cómo se corrigieron |
| :--- | :--- | :--- |
| `platos.html` | 0 errores en el validador. | No hizo falta corregir nada porque las celdas combinadas con `rowspan` y `colspan` cuadraban con las 5 columnas del `<colgroup>`. |
| `contacto.html` | `Error: The first option element in a select element with a required attribute must have an empty value attribute.` | Le quité el atributo `required` al `<select>` porque ya tiene la primera opción marcada por defecto con `selected` (`fix(contacto)`). |
| `index.html` | 0 errores en el validador. | El enlace nuevo a `contacto.html` validó sin errores a la primera. |

### Qué he hecho en esta unidad
En esta unidad he añadido una tabla de datos completa en `platos.html` usando `<caption>`, `<colgroup>`, `<thead>`, `<tbody>` y `<tfoot>`, combinando celdas con `rowspan` y `colspan` y poniendo `scope` en las cabeceras. También he creado el formulario de `contacto.html` con `method="post"`, dividido en dos `<fieldset>` con su `<legend>`, incluyendo los 8 tipos de controles pedidos (`text`, `email`, `tel`, `select`, `radio`, `checkbox`, `textarea`, `submit` y `reset`) con sus `<label for="...">` y atributos de validación. Finalmente he enlazado `contacto.html` desde el `index.html`, he hecho la prueba con `get` y he validado todas las páginas en el W3C hasta dejarlas con 0 errores.

---

## Tarea 6-7 · HTML5 semántico y CSS en mi proyecto web

### Palabra del día (19/11/2026)
semántica

### Reto 1 · Estructura semántica HTML5
En este reto he transformado `index.html`, `platos.html`, `historia.html` y `contacto.html` para cumplir rigurosamente el estándar del Tema 6:
- Eliminación de todos los contenedores `<div>` que se utilizaban únicamente como cajas de maquetación y de cualquier etiqueta o atributo de presentación antiguo (`<center>`, `<font>`, atributos `align`, `bgcolor`, etc.).
- Incorporación de la cabecera semántica `<header>` que agrupa el título/logo del sitio y la barra de navegación `<nav>` con la lista de enlaces del mapa web (`index.html`, `platos.html`, `historia.html`, `contacto.html`).
- Un único elemento `<main>` por documento que engloba el contenido principal.
- Organización del contenido en múltiples elementos `<section>` temáticos y `<article>` con sentido e independencia conceptual (platos del catálogo, recetas, hitos históricos, fichas técnicas y reflexiones).
- Elemento `<aside>` en cada página con información complementaria, notas curiosas, sugerencias de maridaje y recomendaciones.
- Pie de página semántico `<footer>` unificado en todas las páginas con la firma identificativa obligatoria: `<p id="firma-zombneitor123">&copy; 2026 zombneitor123</p>`.
- Metadatos obligatorios en todas las cabeceras: `<!DOCTYPE html>`, `<html lang="es">`, `<meta charset="UTF-8">` y `<meta name="author" content="zombneitor123">`.

### Reto 2 · Formulario con controles HTML5
He enriquecido el formulario de `contacto.html` integrando controles avanzados de HTML5 adaptados a la gestión de talleres gastronómicos y propuestas de recetas:
- **Tipos de input utilizados:**
  1. `email`: para el correo electrónico del participante con validación sintáctica de dominio.
  2. `tel`: teléfono de contacto con validación de patrón numérico (`pattern="[0-9]{9}"`).
  3. `url`: enlace opcional a blog personal o recetario online.
  4. `date`: selector de fecha de inscripción con límites de calendario (`min="2026-11-01" max="2027-06-30"`).
  5. `time`: selector de turno de taller en intervalos de 30 minutos (`min="10:00" max="20:00" step="1800"`).
  6. `number`: número de plazas o comensales a reservar (`min="1" max="10" step="1" value="1"`).
  7. `range`: barra deslizante para indicar el nivel de tolerancia al picante (1 a 5).
  8. `color`: paleta para elegir el color del delantal para el taller presencial (`value="#b03a2e"`).
- **Atributos de validación aplicados:** `placeholder`, `required`, `min`, `max`, `step`, `minlength`, `maxlength` y `autofocus`.
- **Patrones propios con `pattern` y `title` explicativo:**
  - Código de plato: `pattern="P[0-9]{2}"` con `title="El código debe comenzar por una 'P' mayúscula seguida de 2 números (ejemplo: P01, P02, P04)"`.
  - Código postal: `pattern="[0-9]{5}"` con `title="Introduce un código postal español válido de 5 cifras numéricas (ej. 41001)"`.
  - Teléfono: `pattern="[0-9]{9}"` con `title="Introduce un número de teléfono de 9 dígitos (ej. 612345678)"`.
- **Asociación de etiquetas:** Cada uno de los campos cuenta con su etiqueta `<label for="...">` debidamente emparejada con el identificador `id` del control.
- **Elementos `<meter>` y `<progress>`:**
  - `<meter id="aforo-taller" min="0" max="100" low="30" high="75" optimum="50" value="80">80%</meter>`: representa el aforo actual de la sala de catas (80% cubierto, zona de alta ocupación).
  - `<progress id="progreso-plazas" max="20" value="16">16 de 20 plazas</progress>`: indica el avance visual de plazas reservadas para la sesión del sábado (16 de 20 cubiertas).

### Reto 3 · Multimedia y elementos interactivos
- **Vídeo nativo HTML5:** Etiqueta `<video controls poster="media/poster-receta.jpg" width="480">` ubicada en `index.html` con dos fuentes alternativas:
  - `<source src="media/elaboracion-receta.mp4" type="video/mp4">`
  - `<source src="media/elaboracion-receta.webm" type="video/webm">`
  Vídeo real de elaboración y horneado de pizza artesanal, guardado en la carpeta `media/` con un tamaño inferior a 8 MB (cumpliendo el límite de 10 MB).
- **Audio nativo HTML5:** Etiqueta `<audio controls>` con dos fuentes alternativas (`media/taller-podcast.mp3` y `media/taller-podcast.ogg`), que sirve como sintonía musical y cabecera sonora de los talleres culinarios.
- **Vídeo externo incrustado:** Se ha añadido un reproductor de YouTube mediante `<iframe>` con atributos de accesibilidad y modo responsive.
- **Figuras semánticas:** Al menos dos imágenes se han encapsulado mediante `<figure>` y su correspondiente pie de foto descriptivo con `<figcaption>`:
  - `img/comida.jpg`: Panorama culinario general.
  - `img/pizza-napolitana.jpg`: Pizza Margarita al estilo tradicional.
  - `img/sushi-nigiri.jpg`: Bandeja de sushi artesanal con salmón fresco.
- **Preguntas frecuentes interactivas (`<details>` y `<summary>`):**
  - Sección `#preguntas-frecuentes` con cuatro desplegables interactivos.
  - El primer bloque está abierto por defecto mediante el atributo booleano `open`.
  - En las respuestas se han escapado etiquetas HTML utilizando entidades obligatorias: `&lt;plato&gt;`, `&lt;nombre&gt;`, `&lt;precio&gt;`, `&lt;vegetariano/&gt;`, `&lt;main&gt;`, `&lt;section&gt;`, `&lt;article&gt;`, `&lt;aside&gt;`.

### Tema 7 · Hoja de estilos externa (CSS)
Se ha creado el archivo `css/estilos.css`, vinculado mediante `<link rel="stylesheet" href="css/estilos.css">` en el `<head>` de todas las páginas del sitio:
- **Evolución en 3 commits del repositorio:**
  1. `style(css): creacion de hoja de estilos externa con reset tipografia y colores`: variables CSS (`:root`), reseteo universal con `box-sizing: border-box`, paleta de colores temáticos, tipografía legible y barra de navegación flexbox con botones redondeados.
  2. `style(css): reglas para layout semantico tablas multimedia y componentes interactivos`: maquetación de `<main>`, tarjetas para `<article>`, sombreados suaves, bordes temáticos para `<aside>`, estilo completo para tablas (`table`, `th`, `td`, celdas pares e impares, `tfoot`), multimedia responsive y acordeones `<details>`.
  3. `style(css): estilos para formulario controles html5 meter progress y firma`: formateo visual de formularios, pseudo-clases de foco (`:focus`) y validación, diseño para `<meter>` y `<progress>`, botones submit con degradado y selector de firma obligatorio `#firma-zombneitor123`.
- **Selector de firma:**
  ```css
  #firma-zombneitor123 {
    font-size: 1.15rem;
    font-weight: 700;
    color: #ffffff;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    margin-bottom: 0.5rem;
  }
  ```

### Validación W3C (UD6-UD7)

| Página | Validador W3C (HTML5) | Errores detectados | Correcciones realizadas |
| :--- | :--- | :--- | :--- |
| `index.html` | [validator.w3.org](https://validator.w3.org/nu/) | **0 errores, 0 advertencias** | Ninguna; validación limpia a la primera gracias al uso correcto de entidades y jerarquía semántica. |
| `contacto.html` | [validator.w3.org](https://validator.w3.org/nu/) | **0 errores, 0 advertencias** | Ninguna; todos los campos cuentan con su `label for`, `meter`, `progress` y patrones compatibles con el estándar. |
| `platos.html` | [validator.w3.org](https://validator.w3.org/nu/) | **0 errores, 0 advertencias** | Ninguna; la estructura semántica de tabla y artículos valida perfectamente. |
| `historia.html` | [validator.w3.org](https://validator.w3.org/nu/) | **0 errores, 0 advertencias** | Ninguna; cabecera, secciones históricas y lista cronológica libres de errores. |

### Qué he hecho en esta unidad
En esta tarea de evaluación he llevado el proyecto a un nivel profesional combinando los estándares de HTML5 semántico (Tema 6) y la creación de una hoja de estilos externa completa (Tema 7). He sustituido los antiguos bloques `<div>` por etiquetas de significado estructural (`header`, `nav`, `main`, `section`, `article`, `aside`, `footer`), enriquecido el formulario con 8 tipos de inputs HTML5, atributos de validación avanzados, patrones con expresiones regulares y medidores nativos (`meter` y `progress`). También he incorporado contenido multimedia propio en la carpeta `media/` (vídeo en formatos MP4 y WebM con póster, audio en MP3 y OGG) y un vídeo incrustado de YouTube, además de galerías de imágenes con `figure`/`figcaption` y preguntas frecuentes desplegables con `details`/`summary` y entidades escapadas. Por último, he diseñado una hoja de estilos CSS externa organizada y responsiva, con commits convencionales distribuidos y comprobando que todas las páginas del repositorio obtienen 0 errores y 0 advertencias en el validador oficial del W3C.
