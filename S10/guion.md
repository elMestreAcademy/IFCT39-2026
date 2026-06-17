# S10 -- SEO técnico y velocidad

> En las sesiones anteriores trabajamos el SEO de contenido (on-page) y dejamos el sitio midiendo (GA4) y legal (banner de cookies). Hoy va el **tercer pilar**: el SEO técnico. Que Google pueda **rastrear e indexar** el sitio sin tropiezos y que la página **cargue rápido**.
> El trabajo de hoy es medible: arrancamos midiendo la velocidad con PageSpeed, entendemos los Core Web Vitals, y subimos la nota con caché y optimización de imágenes. Objetivo del proyecto: **pasar de 75 en PageSpeed móvil**. Luego repasamos robots.txt, sitemap, canonical y datos estructurados, que Yoast ya nos gestiona casi solo.
> Sesión de 4 h (calendario real: 25 sesiones de 4 h). Esta es la sesión 15.

---

## Objetivos del día

1. Entender qué es el **SEO técnico** y por qué es el tercer pilar, junto al on-page y el off-page.
2. **Medir la velocidad** con PageSpeed Insights y leer los **Core Web Vitals** (LCP, INP, CLS).
3. **Subir la nota** con las dos palancas que más mueven la aguja: **caché** y **optimización de imágenes**. Objetivo: pasar de 75.
4. Saber qué son y dónde están **robots.txt** y el **sitemap**, y comprobar que están bien.
5. Entender el **canonical** y los **datos estructurados** (Schema), y ver que Yoast los pone solo.

---

## Cronograma

| Tramo     | Min | Bloque                                                          |
| --------- | --- | --------------------------------------------------------------- |
| 0:00-0:20 | 20  | Apertura: checkpoint Normativa (banner, consentimiento)         |
| 0:20-0:50 | 30  | Qué es el SEO técnico: rastrear, indexar, ir rápido             |
| 0:50-1:40 | 50  | Velocidad: PageSpeed Insights y Core Web Vitals (hands-on)      |
| 1:40-1:50 | 10  | Descanso                                                        |
| 1:50-2:40 | 50  | Subir la nota: caché + optimizar imágenes, re-medir (hands-on)  |
| 2:40-2:50 | 10  | Descanso                                                        |
| 2:50-3:30 | 40  | robots.txt, sitemap, canonical y datos estructurados            |
| 3:30-4:00 | 30  | Cierre, deberes y conexión con S11                              |

---

## Apertura: checkpoint Normativa

Cada uno verifica en su WP mientras paso lista de estado:

1. **El banner de cookies aparece** en incógnito, y rechazar funciona? (deber de la sesión anterior).
2. **GA4 bajo consentimiento**: tras aceptar, la visita cae en Tiempo real. Tras rechazar, no.
3. **Aviso legal con datos completos**, sin huecos. Quien lo dejara a medias, lo remata en paralelo.

Y de paso: ha entrado **tráfico real** estos días? Lo miramos un segundo en GA4 > Adquisición. Ya tiene sentido empezar a ver canales.

---

## Qué es el SEO técnico

El SEO tiene tres patas y hoy va la tercera:

- **On-page** (ya hecho): el contenido, los títulos, las palabras clave, el enlazado interno.
- **Off-page** (lo veremos): enlaces que apuntan a mi sitio, autoridad, reputación.
- **Técnico** (hoy): que el sitio sea **fácil de rastrear, fácil de indexar y rápido**.

Tres preguntas que responde el SEO técnico:

- **Puede Google entrar y leerlo?** robots.txt, sitemap, que no haya bloqueos.
- **Entiende qué es cada cosa?** canonical (cuál es la URL buena), datos estructurados (qué tipo de contenido es).
- **Carga rápido?** Core Web Vitals. Google usa la velocidad como factor de posicionamiento, y sobre todo: una página lenta pierde visitas antes de cargar.

La buena noticia: en WordPress con Yoast, buena parte de esto ya está hecho. Hoy lo **comprobamos y lo afinamos**, no lo construimos de cero. Donde sí hay trabajo de verdad es en la velocidad.

---

## Velocidad: medir primero

No se optimiza lo que no se mide. Empezamos midiendo.

### PageSpeed Insights

1. Ir a `pagespeed.web.dev` y pegar la URL del sitio.
2. Mirar las dos pestañas: **Móvil** y **Escritorio**. La de móvil suele dar peor; es la que cuenta, porque la mayoría del tráfico es móvil.
3. Leer la **nota de 0 a 100** (la bola de Rendimiento), los **Core Web Vitals** y la sección **Oportunidades** (qué arreglar y cuánto se ganaría).

Que cada uno mida su sitio y apunte la nota de partida. Luego comparamos al final.

### Core Web Vitals

Las tres métricas que Google mira de la experiencia real:

| Métrica | Qué mide                                              | Buena cuando |
| ------- | ----------------------------------------------------- | ------------ |
| LCP     | Cuánto tarda en verse el elemento más grande          | < 2,5 s      |
| INP     | Cómo de rápido responde el sitio al interactuar       | < 200 ms     |
| CLS     | Cuánto "baila" el contenido mientras carga            | < 0,1        |

Traducido: **LCP** es "tarda en aparecer", **INP** es "tarda en reaccionar", **CLS** es "se mueve y hago clic donde no quería". Las tres se notan en sitios cargados de imágenes pesadas y plugins de más.

---

## Subir la nota

En un WordPress de aula, casi toda la mejora viene de **dos palancas**: imágenes y caché. Vamos a por ellas y re-medimos.

### Caché

La caché guarda una versión ya montada de la página para no rehacerla en cada visita. Es lo que más sube la nota de golpe.

1. Instalar un plugin de caché. Sirve el del propio hosting si lo ofrece, o `LiteSpeed Cache` / `WP Super Cache`.
2. Activar la **caché de página** (lo básico, casi siempre con activarlo basta).
3. Con cuidado: la **minificación** de CSS/JS también ayuda, pero a veces rompe el diseño. Se activa de una en una y se comprueba el sitio después de cada cambio.

### Imágenes

Las imágenes pesadas son el problema número uno del LCP.

1. Instalar un plugin de compresión: `Smush` o `EWWW Image Optimizer`.
2. **Comprimir** las imágenes ya subidas (bulk) y servirlas en formato moderno **WebP**.
3. **Lazy load**: WordPress ya lo trae de serie (carga las imágenes según se bajan). Solo comprobar que no se haya desactivado.
4. Norma de aquí en adelante: no subir imágenes de 4000 px para un hueco de 600. Redimensionar antes de subir.

### Re-medir

Volver a `pagespeed.web.dev`, misma URL, móvil. La nota debería subir. **Objetivo: pasar de 75.** Quien no llegue, miramos juntos las "Oportunidades" que le quedan.

---

## robots.txt, sitemap, canonical y datos estructurados

La parte de "que Google entienda el sitio". Aquí Yoast hace casi todo; nosotros comprobamos.

### robots.txt

- Es un archivo con **instrucciones para los rastreadores**: por dónde pueden pasar y por dónde no.
- Está en `tudominio.com/robots.txt`. Lo abrimos en el navegador y lo miramos.
- Cuidado con `Disallow`: si bloquea algo que queremos indexar, Google no entra. En un sitio normal no hay que tocarlo.

### Sitemap

- Es la **lista de URLs** que le damos a Google para que las encuentre. Ya lo enviamos en S08 (`sitemap_index.xml`, de Yoast).
- Yoast lo mantiene solo: cada vez que publicamos algo, lo añade. Solo recordamos dónde está.

### Canonical

- Cuando el mismo contenido vive en varias URLs (con barra y sin barra, con parámetros, paginado), la etiqueta **canonical** le dice a Google **cuál es la buena**.
- Yoast la pone sola, apuntando cada página a sí misma. Lo comprobamos: en el navegador, `Ver código fuente` y buscar `rel="canonical"`.

### Datos estructurados (Schema)

- Es un vocabulario que le dice a Google **qué es** cada cosa: un artículo, un producto, una FAQ, un negocio local.
- Permite los **resultados enriquecidos** en Google: estrellas de valoración, FAQ desplegables, migas de pan.
- Yoast añade los básicos solo (sitio, organización, artículo, migas). Para afinar: en `Yoast > Ajustes`, indicar si el sitio es de una **organización** o una **persona**.
- Comprobarlo con el **Rich Results Test** de Google: pegar la URL y ver qué tipos detecta.

---

## Cierre

### Qué tienen hoy

- El sitio medido en PageSpeed, con la nota de móvil por encima de 75.
- Caché activada y las imágenes comprimidas en WebP.
- Saben qué hacen robots.txt y el sitemap, y los han comprobado.
- Entienden el canonical y los datos estructurados, y han visto que Yoast los pone solos.

### Deberes para la próxima

1. **Dejar el sitio por encima de 75** en PageSpeed móvil. Quien no llegara hoy, rematar las imágenes pesadas que queden.
2. Comprobar en casa el **robots.txt** y el **canonical** de la Landing (ver código fuente).
3. Para S11, traer una **lista de 10-15 palabras o frases** por las que querrían que su sitio apareciera en Google. Es la materia prima del keyword research.

### Próxima sesión: keyword research, contenido y GEO

Con el sitio rápido y rastreable, toca atraer a la gente correcta. La próxima trabajamos la **investigación de palabras clave** (intención de búsqueda, clusters), un repaso de contenido y E-E-A-T, y el **GEO**: cómo posicionar también en ChatGPT, Gemini y Perplexity. Es el cierre del Módulo 1.

---

## Recursos

- [PageSpeed Insights](https://pagespeed.web.dev/)
- [Core Web Vitals (web.dev)](https://web.dev/articles/vitals)
- [Largest Contentful Paint, explicado](https://webenso.com/how-to-find-the-lcp-largest-contentful-paint-html-element/)
- [Rich Results Test (Google)](https://search.google.com/test/rich-results)
- [Schema.org](https://schema.org/)
- [Yoast SEO - ayuda](https://yoast.com/help/)
