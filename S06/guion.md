# S06 -- Primer contacto con WordPress + plugins SEO

## Objetivos del dia

1. Que cada alumno tenga su WordPress operativo y se mueva por el panel.
2. Instalar y configurar un plugin SEO (Yoast o Rank Math).
3. Entender la diferencia entre **paginas** y **entradas** y crear su primera pieza de contenido.
4. Consolidar el criterio de "proyecto posicionable" (bloque pendiente de S05).

---

## Cronograma

| Tramo     | Min | Bloque                                                        |
| --------- | --- | ------------------------------------------------------------- |
| 0:00-0:20 | 20  | Apertura: repaso S05, estado de proyectos y accesos WP        |
| 0:20-0:50 | 30  | Que hace posicionable un proyecto (bloque movido de S05)      |
| 0:50-1:30 | 40  | Recorrido por el panel de administracion de WordPress         |
| 1:30-1:40 | 10  | Descanso                                                      |
| 1:40-2:30 | 50  | Instalar y configurar Yoast SEO / Rank Math                   |
| 2:30-3:20 | 50  | Paginas vs entradas + crear contenido con el editor Gutenberg |
| 3:20-3:30 | 10  | Descanso                                                      |
| 3:30-4:40 | 70  | Trabajo individual: 1 pagina + 1 entrada en su propio WP      |
| 4:40-5:00 | 20  | Cierre, deberes y conexion con S07                            |

---

## Apertura

- Repaso rapido de S05: lienzo de proyecto, validacion de nicho.
- Confirmar que cada alumno tiene acceso a su WordPress (`wpN.masterfactories.com`).
- Quien no cerro idea propia en S05 recibe un WordPress generico hoy -- nadie se queda sin sandbox.

---

## Que hace posicionable un proyecto

La idea no tiene que ser perfecta; tiene que **dar juego para el curso**. Criterios:

- **Tiene busquedas**: alguien escribe eso en Google/ChatGPT. Si nadie lo busca, no hay SEO que hacer.
- **Acotado**: "recetas" es imposible; "recetas sin gluten para opositores" se posiciona.
- **Tienes algo que aportar**: experiencia, producto, ganas. El SEO premia el contenido real.
- **Objetivo claro**: informar / vender / marca personal / captar leads. Eso decide el tipo de web.

corto (5 min): cada uno dice en voz alta su nicho y el grupo evalua si cumple los 4 criterios.

---

## Recorrido por el panel de WordPress

Hacer la demo en pantalla sobre un WP propio; que sigan en el suyo.

### Zonas que veremos hoy

| Zona              | Para que sirve                                            |
| ----------------- | --------------------------------------------------------- |
| Escritorio        | Resumen del estado del sitio                              |
| Entradas          | Blog: artículos ordenados por fecha                       |
| Paginas           | Contenido estatico: Inicio, Sobre mi, Contacto            |
| Apariencia        | Temas, menus, widgets                                     |
| Plugins           | Extensiones que amplian la funcionalidad                  |
| Ajustes > General | Titulo del sitio, tagline, zona horaria                   |
| Ajustes > Lectura | Pagina de inicio estatica o blog                          |
| Ajustes > URLs    | Estructura de los permalinks (importante para SEO)        |

**Accion:** `Ajustes > URLs` -- cambiar el permalink a `/%postname%/` si no lo esta ya.
Es la configuracion mas basica de SEO on-page que afecta a todas las URLs del sitio.

---

## Instalar plugins

### Como se instala un plugin

`Plugins > Añadir nuevo > buscar > Instalar > Activar`

### Plugin SEO: Yoast SEO o Rank Math

Ambos son gratuitos y validos. Para el curso usaremos **Yoast SEO** (mas conocido; mas documentacion en castellano).

**Configuracion minima de Yoast tras instalar:**

1. Asistente de configuracion: tipo de sitio, nombre del autor, paginas de privacidad y sitemap.
2. `SEO > General > Caracteristicas`: activar XML Sitemaps.
3. `SEO > Apariencia en buscadores > Tipos de contenido`: revisar que entradas y paginas estan indexadas.

### Otros plugins que veremos mas adelante (no instalar hoy)

- **Site Kit by Google** (GA4 + Search Console) -- S07
- **WP Super Cache / LiteSpeed Cache** (velocidad) -- SEO tecnico
- **Complianz / CookieYes** (GDPR / cookies) -- cuando conectemos GA4

---

## Paginas vs entradas

| Concepto   | Paginas                                   | Entradas                              |
| ---------- | ----------------------------------------- | ------------------------------------- |
| Naturaleza | Contenido estatico                        | Contenido cronologico (blog)          |
| URL tipica | `/sobre-mi/`, `/contacto/`                | `/categoria/titulo-del-articulo/`     |
| SEO        | Paginas clave del sitio (jerarquia)       | Contenido fresco, keywords de cola larga |
| Ejemplos   | Inicio, Servicios, Sobre mi, Contacto     | Articulos, guias, noticias            |

**Para SEO necesitamos las dos cosas**: paginas bien estructuradas + contenido fresco en entradas.

### El editor Gutenberg (bloques)

Demo de 10 min:
- Bloques basicos: parrafo, titulo (H2/H3), imagen, lista, cita.
- Usar titulos H2/H3 con las keywords del proyecto -- conexion directa con lo que veremos en SEO on-page.
- El panel lateral de Yoast: semaforo de SEO y legibilidad.

---

## Trabajo individual

Cada alumno crea en su WordPress:

1. **Una pagina estatica**: "Sobre mi" o "Sobre el proyecto" (minimo 150 palabras, con H2).
2. **Una entrada de blog**: tema libre relacionado con su nicho (minimo 200 palabras, con H2 y una imagen).

Mientras trabajan, rotar mesa por mesa para ayudar y revisar que Yoast este activo y configurado.

---

## Cierre -- Deberes y conexion con S07

1. Terminar las dos piezas de contenido si no lo acabaron en clase.
2. Traer 3 ideas de titulos de entradas para su proyecto (pensados para SEO, no para redes sociales).
3. S07: **Google Search Console** -- conectar el sitio, verificar propiedad, primer informe.

---

## Recursos

- [Yoast SEO -- Guia de inicio (castellano)](https://yoast.com/help/)
- [Editor Gutenberg (WordPress.org)](https://wordpress.org/documentation/article/wordpress-editor/)
- [Estructura de URLs en WordPress (Yoast)](https://yoast.com/help/changing-the-url-structure/)
