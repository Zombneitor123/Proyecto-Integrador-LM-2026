# Proyecto Integrador LM 2026

- **Nombre**: Manuel Alonso Bono Torres
- **Usuario de GitHub**: Zombneitor123
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
| `index.html` | Inicio \| Comida Internacional | Portada: presentación del proyecto, introducción a las tradiciones e ingredientes, platos favoritos, ficha técnica en `<pre>` y cita gastronómica en `<blockquote>`. |
| `platos.html` | Platos \| Comida Internacional | Catálogo completo con todos los platos de `datos.xml` (`Pizza Margarita`, `Sushi de Salmón` y `Tacos al Pastor`), incluyendo su ID, origen, precio en euros, categoría e ingredientes. |
| `historia.html` | Historia \| Comida Internacional | Orígenes e historia cultural de las tres grandes cocinas del proyecto (Italia, Japón y México), técnicas tradicionales y cita histórica sobre patrimonio culinario. |
| `contacto.html` | Contacto \| Comida Internacional | Datos de contacto del proyecto, horarios de atención y colaboraciones en formato `<pre>`, reseñas de lectores en `<blockquote>` y preguntas frecuentes. |

### Validación W3C

| Página | Errores detectados por el validador W3C | Cómo se corrigieron |
| :--- | :--- | :--- |
| `index.html` | 0 errores (ningún error ni advertencia en la validación). | No fue necesario realizar correcciones porque la estructura de bloques, títulos y entidades era válida desde el inicio. |
| `platos.html` | 0 errores (ningún error ni advertencia en la validación). | No necesitó correcciones; los caracteres `<` y `>` dentro del bloque `<pre>` ya estaban escapados con `&lt;` y `&gt;`. |
| `historia.html` | `Error: The width attribute on the hr element is obsolete. Use CSS instead.` | Se eliminó el atributo obsoleto `width="80%"` de la etiqueta `<hr>`, dejándola como `<hr>` limpia (`fix(historia)`). |
| `contacto.html` | 0 errores (ningún error ni advertencia en la validación). | No fue necesario realizar correcciones; el documento validó con 0 errores a la primera. |

### Qué he hecho en esta unidad
En esta unidad he transformado mi página inicial en un sitio web completo de cuatro páginas sobre comida internacional siguiendo un mapa del sitio definido en el `README.md`. He completado la cabecera `<head>` con todos sus metadatos, estructurado el cuerpo de cada documento mediante una jerarquía de títulos sin saltos (`h1`, `h2` y `h3`) y agrupado las secciones en bloques `<div>` comentados con sangría coherente. Además, he incorporado citas con `<blockquote>`, fichas alineadas en `<pre>`, entidades HTML nominales y numéricas, volcado todos los elementos de `datos.xml` en `platos.html` y validado todo el sitio en el validador del W3C hasta lograr 0 errores.
