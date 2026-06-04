# S03 — HTML + Cómo se construye una web

---

## Objetivos del día

---

### Chuleta completa de Markdown

| Elemento               | Sintaxis Markdown                       | resultado HTML              |
| ---------------------- | --------------------------------------- | --------------------------- |
| Texto normal           | `Texto`                                 | La mayor parte del copy     |
| Encabezado 1           | `# Título`                              | `<h1>` — título principal   |
| Encabezado 2           | `## Título`                             | `<h2>`                      |
| Encabezado 3–6         | `### … ######`                          | `<h3>` … `<h6>`             |
| Negrita                | `**texto**` / `__texto__`               | `<strong>`                  |
| Cursiva                | `*texto*` / `_texto_`                   | `<em>`                      |
| Negrita + cursiva      | `***texto***`                           | `<strong><em>`              |
| Tachado                | `~~texto~~`                             | `<del>`                     |
| Lista sin orden        | `- elemento` / `* elemento`             | `<ul><li>`                  |
| Lista numerada         | `1. elemento`                           | `<ol><li>`                  |
| Lista anidada          | `··- elemento` (2 espacios)             | sub-lista                   |
| Lista de tareas        | `- [ ] pendiente` / `- [x] hecho`       | checkbox                    |
| Enlace                 | `[texto](https://url.com)`              | `<a href>`                  |
| Enlace con tooltip     | `[texto](url "título")`                 | `<a title>`                 |
| Imagen                 | `![alt](imagen.jpg)`                    | `<img alt>`                 |
| Cita                   | `> texto`                               | `<blockquote>`              |
| Cita anidada           | `>> texto`                              | anidación                   |
| Código en línea        | `` `código` ``                          | `<code>`                    |
| Bloque de código       | ` ```js … ``` `                         | `<pre><code>` con coloreado |
| Separador              | `---` / `***`                           | `<hr>`                      |
| Tabla                  | `\| col \| col \|` + `\| --- \| --- \|` | `<table>`                   |
| Escapar carácter       | `\*`, `\#`, `\[`…                       | muestra el símbolo tal cual |
| Salto de línea forzado | dos espacios al final de línea          | `<br>`                      |

### Objetivos del día (2 min)

1. Cubrir **HTML básico** (pendiente de S02): esqueleto, etiquetas, etiquetas que mueven el SEO.
2. Entender el ciclo **petición → servidor → HTML → navegador** y qué es el **DOM**.
3. Saber qué son **dominio, DNS y hosting** y cómo afectan al SEO técnico.
4. Primer vistazo a **CSS** (solo el concepto; no hace falta profundizar).
5. _(Si hay tiempo)_ Cada alumno empieza a definir su proyecto.

---

### Esqueleto mínimo HTML

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Mi primera página</title>
  </head>
  <body>
    <h1>Hola mundo</h1>
    <p>Mi primer párrafo.</p>
  </body>
</html>
```

Abrir el archivo en el navegador. Luego abrirlo en [w3schools Tryit](https://www.w3schools.com/tryit/) para que todos puedan editar a la vez.

- `<head>` = información para el navegador y para Google (no se ve en página).
- `<body>` = lo que sí se ve.

### Etiquetas básicas

```html
<h1>…</h1>
…
<h6>…</h6>
<!-- encabezados, jerarquía -->
<p>párrafo</p>
<strong>importante</strong> <em>énfasis</em>
<a href="https://ejemplo.com">enlace</a>
<img src="foto.jpg" alt="descripción" />
<ul>
  <li>viñeta</li>
</ul>
<ol>
  <li>numerada</li>
</ol>
<br />
<hr />
```

**Paralelismo con Markdown** (refuerza lo de ayer):

| Markdown       | HTML                          |
| -------------- | ----------------------------- |
| `# Título`     | `<h1>Título</h1>`             |
| `**negrita**`  | `<strong>negrita</strong>`    |
| `[texto](url)` | `<a href="url">texto</a>`     |
| `![alt](img)`  | `<img src="img" alt="alt" />` |

### Ejemplo de S02 a S03

**Tarea:** convertir la mini-ficha de Markdown de S02 a HTML. Si no se hizo la ficha, crearla ahora en HTML directamente.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Nombre Apellido</title>
  </head>
  <body>
    <h1>Nombre Apellido</h1>
    <p>Una frase de quién soy.</p>
    <h2>Lo que sé hacer</h2>
    <ul>
      <li>Habilidad 1</li>
      <li>Habilidad 2</li>
    </ul>
    <h2>Contacto</h2>
    <p><a href="mailto:correo@ejemplo.com">correo@ejemplo.com</a></p>
  </body>
</html>
```

---

### HTML semántico

```html
<header>…</header>
<!-- cabecera -->
<nav>…</nav>
<!-- menú -->
<main>
  <section>…</section>
  <article>…</article>
</main>
<footer>…</footer>
<!-- pie -->
```

![HTML Semántico](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/tutorial/html-semantic-tags/semantic-tags.png)


> Google entiende mejor una página bien estructurada → mejor SEO **y** mejor accesibilidad.

### Las etiquetas que mueven el SEO

| Etiqueta                    | Para qué                            | Regla rápida                    |
| --------------------------- | ----------------------------------- | ------------------------------- |
| `<title>`                   | Título en pestaña y en Google       | Único por página, ~50–60 car.   |
| `<meta name="description">` | Resumen bajo el resultado en Google | ~150 car., atractivo            |
| `<h1>`                      | Tema principal de la página         | **Uno solo** por página         |
| `<h2>`–`<h6>`               | Jerarquía del contenido             | En orden, sin saltos            |
| `alt` en `<img>`            | Describe la imagen                  | Accesibilidad + SEO de imágenes |
| `lang` en `<html>`          | Idioma                              | `es`                            |

```html
<head>
  <meta charset="UTF-8" />
  <title>Zapatillas running baratas | MiTienda</title>
  <meta
    name="description"
    content="Compra zapatillas de running con envío 24h."
  />
</head>
```

### Práctica: mejorar la ficha (15 min)

Añadir a la ficha de antes:

- `title` y `meta description` descriptivos.
- Un único `<h1>`.
- Una imagen con `alt` bien redactado.
- Envolver en `<header>` / `<main>` / `<footer>`.

---

## 2:30 · Cómo funciona la web (50 min)

### El ciclo petición-respuesta (15 min)

```plaintext
Navegador
  │── escribe URL ──▶ DNS ──▶ IP del servidor
  │◀────────── HTML + CSS + JS ──────────────
  │── renderiza la página
```

1. Escribes `www.ejemplo.com` → el navegador pregunta al **DNS** cuál es la IP.
2. El servidor responde con el fichero **HTML**.
3. El navegador lee el HTML, pide el CSS, construye el **DOM** y pinta la página.

> **Por qué importa al SEO:** Googlebot hace exactamente esto. Si el servidor tarda, si el HTML no llega limpio, Google lo penaliza.

### El DOM

DOM = Document Object Model. Es el árbol de nodos que el navegador construye a partir del HTML.

```plaintext
html
 ├── head
 │    ├── title
 │    └── meta
 └── body
      ├── h1
      ├── p
      └── a
```

- CSS y JavaScript manipulan el DOM (sin tocar el archivo HTML original).
- Las herramientas de SEO técnico leen el DOM, no el HTML fuente → importante para páginas con JavaScript pesado.

### DevTools — «Inspeccionar elemento»

Abrir el navegador en cualquier página conocida → clic derecho → _Inspeccionar_.

Mostrar:

- Pestaña **Elements**: el DOM en vivo.
- Pestaña **Network**: las peticiones (cuánto tarda cada recurso).
- Buscar el `<title>` y el `<meta name="description">` de la página.

**Ejercicio rápido:** inspeccionar la web de uno de sus proyectos (o la de un competidor) y encontrar el `<h1>` y el `<title>`.

> _Esto es exactamente lo que hace una auditoría SEO on-page_
