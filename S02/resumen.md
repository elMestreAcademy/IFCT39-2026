# S02

## Notas y links

### Links

- [is-markdown-taking-over?](https://www.hendrik-erz.de/post/is-markdown-taking-over)

## Guión

### Objetivos del día

1. Entender qué es **HTML**, cómo se estructura una página y **qué etiquetas importan para SEO** (anticipo de S04).
2. Escribir **Markdown** con soltura: encabezados, listas, enlaces, imágenes, tablas, código.
3. Ver la relación entre ambos: **Markdown se convierte en HTML**.
4. Quitar el miedo al código a los perfiles no técnicos (y dar reto a los técnicos).

---

### Cronograma (5 h)

| Tramo     | Min | Bloque                                                                    |
| --------- | --- | ------------------------------------------------------------------------- |
| 0:00-0:20 | 20  | Apertura: repaso S01 + "deberes del profe" (caída de YouTube) + objetivos |
| 0:20-1:30 | 70  | **Markdown** (teoría exprés + práctica en vivo)                           |
| 1:30-1:40 | 10  | Descanso                                                                  |
| 1:40-3:10 | 90  | **HTML I**: cómo funciona + etiquetas básicas                             |
| 3:10-3:20 | 10  | Descanso                                                                  |
| 3:20-4:30 | 70  | **HTML II**: estructura semántica + etiquetas SEO + práctica              |
| 4:30-5:00 | 30  | Cierre: retos por nivel, recap y deberes                                  |

---

### 0:00 · Apertura (20 min)

- **Repaso S01:** SEO vs SEM, KPIs (CPM/CPC, QS, subasta) GEO
- **Deberes del profe** (los de S01): comentar 2-3 min la caída de ingresos/vistas de YouTube -> Cómo cambia el ecosistema (gancho de S01).
- **Objetivos del día**  HTML + Markdown

---

### 0:20 · Markdown (70 min)

**Idea:** Markdown es texto plano con marcas simples que se convierte en HTML con formato. Lo lee una persona y lo entiende una máquina.

#### Demo en vivo (editor)

Abrir un editor con vista previa en directo:

- [markdownlivepreview.com](https://markdownlivepreview.com/) · [StackEdit](https://stackedit.io/) · o **VS Code** (`Ctrl+K V`).

#### Chuleta de Markdown

````markdown
# Título 1

## Título 2

### Título 3

Texto normal con **negrita** y _cursiva_.

- Lista
- con viñetas
  - y sub-viñetas

1. Lista
2. numerada

[Texto del enlace](https://ejemplo.com)
![Texto alternativo de la imagen](imagen.jpg)

> Cita / nota destacada.

`código en línea`

​`js
// bloque de código
console.log("hola");
​`

| Columna A | Columna B |
| --------- | --------- |
| dato 1    | dato 2    |

--- (línea separadora)
````

#### Práctica guiada (todos a la vez)

Escribir una **mini-ficha personal** en Markdown (neutra, sin ser el proyecto):

```markdown
## Nombre Apellido

Una frase de quién soy.

### Lo que sé hacer

- Tema 1
- Tema 2

### Contacto

[Email](mailto:tucorreo@ejemplo.com)
```

> **Gancho IA:** Markdown es el formato en el que mejor "piensan" los LLM. Pedirle a un modelo _"dame la respuesta en Markdown con encabezados y tabla"_ mejora muchísimo el resultado.

---

### 1:40 · HTML I - Cómo funciona y etiquetas básicas (90 min)

**Idea:** HTML (HyperText Markup Language) es el **esqueleto** de toda página. El navegador lo lee y lo "dibuja". Las marcas se llaman **etiquetas**: `<etiqueta>contenido</etiqueta>`.

#### Esqueleto mínimo de una página

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

- `<head>` = información para el navegador y para Google (no se ve en la página).
- `<body>` = lo que sí se ve.

#### Etiquetas básicas (demo en w3schools "Try it")

```html
<h1>…</h1>
…
<h6>…</h6>
<!-- encabezados, jerarquía -->
<p>párrafo</p>
<strong>importante</strong> <em>énfasis</em>
<a href="https://ejemplo.com">enlace</a>
<img src="foto.jpg" alt="descripción de la foto" />
<ul>
  <li>viñeta</li>
</ul>
<ol>
  <li>numerada</li>
</ol>
<br />
<hr />
```

- Probarlo en el editor en vivo: [w3schools Tryit](https://www.w3schools.com/tryit/).
#- **Paralelismo con Markdown:** `#` ↔ `<h1>`, `**` ↔ `<strong>`, `[]( )` ↔ `<a>`, `![]( )` ↔ `<img>`. _Markdown es un atajo para escribir HTML._

#### Práctica guiada

Convertir la **mini-ficha de Markdown** del bloque anterior a **HTML** copiando el esqueleto y rellenándolo. (Parejas técnico/no-técnico.)

---

### 3:20 · HTML II - Semántica y etiquetas SEO (70 min)

#### HTML semántico (estructura con significado)

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

Google entiende mejor una página bien estructurada -> mejor SEO y mejor accesibilidad.

#### Las etiquetas que SÍ mueven el SEO

| Etiqueta                    | Para qué                            | Regla rápida                    |
| --------------------------- | ----------------------------------- | ------------------------------- |
| `<title>`                   | Título en la pestaña y en Google    | Único por página, ~50-60 car.   |
| `<meta name="description">` | Resumen bajo el resultado en Google | ~150 car., atractivo            |
| `<h1>`                      | Tema principal de la página         | **Uno solo** por página         |
| `<h2>`-`<h6>`               | Jerarquía del contenido             | En orden, sin saltos            |
| `alt` en `<img>`            | Describe la imagen                  | Accesibilidad + SEO de imágenes |
| `lang` en `<html>`          | Idioma de la página                 | `es`                            |

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

#### Práctica final

Mejorar la ficha HTML: `title` + `meta description` correctos, un único `<h1>`, una imagen con `alt`, y envolverla en `<header>/<main>/<footer>`.

---

### 4:30 · Cierre - Retos por nivel + deberes (30 min)

#### Retos en clase (según perfil de `alumnos.md`)

- **Base (todos):** mini-ficha en Markdown + esqueleto HTML que se vea en el navegador.
- **Intermedio (Rosa, Ysabel, Carlos, Celia):** añadir lista, enlace, imagen con `alt` y una tabla; encabezados bien jerarquizados.
- **Avanzado (Ricardo, Gustavo, César):** HTML semántico completo + meta tags SEO + **validar en** [validator.w3.org](https://validator.w3.org/) + anotar 3 cosas que cambiarían para posicionar mejor.

#### Deberes que me gustaria que hicieras

1. Pasar **tus apuntes de hoy a Markdown** (1 archivo `.md`).
2. Escribir **una página HTML** de un tema que te interese (mín.: `title`, `meta description`, un `<h1>`, 2 párrafos, 1 imagen con `alt`, 1 enlace).
3. _(Opcional técnicos)_ recorrer la rama _Frontend_ de [roadmap.sh](https://roadmap.sh/) y traer dudas.

---

### Conexión con el temario

- `title` / `meta` / `<h1>` / `alt` -> **SEO on-page** (S04-S05).
- HTML semántico y validación -> **técnicas en programación** (S05).
- Markdown como formato para LLM -> **GEO** (S10) y **laboratorio de IA** (S19).

### Recursos

- [w3schools HTML](https://www.w3schools.com/html/) · [Tryit editor](https://www.w3schools.com/tryit/)
- [Markdown Live Preview](https://markdownlivepreview.com/) · [Guía Markdown](https://www.markdownguide.org/basic-syntax/)
- [roadmap.sh](https://roadmap.sh/) · [Validador W3C](https://validator.w3.org/)
