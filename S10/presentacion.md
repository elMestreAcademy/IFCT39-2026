---
marp: true
paginate: true
---

# SEO técnico y velocidad

Sesión S10

---

## Estado esperado

El sitio ya mide y ya es legal. Hoy va el tercer pilar del SEO: el técnico. Al finalizar conseguiremos:

- El sitio medido en PageSpeed, con la nota de móvil por encima de 75.
- Caché activada y las imágenes comprimidas.
- Saber qué hacen robots.txt, sitemap y canonical, y haberlos comprobado.
- Entender los datos estructurados y ver que Yoast los pone solos.

---

## Requisitos de sesiones anteriores

- El banner de cookies funcionando y GA4 bajo consentimiento (Normativa).
- El sitio dado de alta en Search Console, con sitemap enviado (S08).
- La Landing y las páginas publicadas, con su on-page.

Si falta algo, eso es lo primero de hoy.

---

## Los tres pilares del SEO

- **On-page** (ya hecho): contenido, títulos, palabras clave, enlazado interno.
- **Off-page** (lo veremos): enlaces hacia el sitio, autoridad, reputación.
- **Técnico** (hoy): que el sitio sea fácil de rastrear, fácil de indexar y rápido.

Hoy comprobamos y afinamos lo técnico; en velocidad sí hay trabajo de verdad.

---

## Qué responde el SEO técnico

- **Puede Google entrar y leerlo?** robots.txt, sitemap, sin bloqueos.
- **Entiende qué es cada cosa?** canonical y datos estructurados.
- **Carga rápido?** Core Web Vitals.

Una página lenta pierde visitas antes incluso de cargar.

---

## Medir primero

No se optimiza lo que no se mide.

1. Vamos a `pagespeed.web.dev` y pegamos la URL del sitio.
2. Miramos las dos pestañas: **Móvil** y **Escritorio**. La de móvil es la que cuenta.
3. Leemos la nota de 0 a 100, los Core Web Vitals y la sección **Oportunidades**.

Apuntamos la nota de partida para comparar al final.

---

## Core Web Vitals

| Métrica | Qué mide                            | Buena cuando |
| ------- | ----------------------------------- | ------------ |
| LCP     | Tarda en verse lo más grande        | < 2,5 s      |
| INP     | Tarda en reaccionar al interactuar  | < 200 ms     |
| CLS     | Cuánto baila el contenido al cargar | < 0,1        |

Las tres empeoran con imágenes pesadas y plugins de más.

---

## Subir la nota: caché

La caché guarda la página ya montada para no rehacerla en cada visita. Es lo que más sube la nota de golpe.

1. Instalamos un plugin de caché: el del hosting, o LiteSpeed Cache / WP Super Cache.
2. Activamos la **caché de página**.
3. La minificación de CSS/JS también ayuda, pero a veces rompe el diseño: la activamos de una en una y comprobamos.

---

## Subir la nota: imágenes

Las imágenes pesadas son el problema número uno del LCP.

1. Instalamos un plugin de compresión: Smush o EWWW.
2. Comprimimos las imágenes y las servimos en formato **WebP**.
3. El **lazy load** ya viene de serie en WordPress: solo comprobamos que esté activo.
4. Norma: no subir imágenes enormes para huecos pequeños.

---

## Re-medir

Volvemos a `pagespeed.web.dev`, misma URL, móvil.

La nota debería subir. **El objetivo es pasar de 75.** Quien no llegue, miramos juntos las Oportunidades que le queden.

---

## robots.txt y sitemap

- **robots.txt**: instrucciones para los rastreadores. Está en `tudominio.com/robots.txt`. Cuidado con `Disallow`: no bloquear lo que queremos indexar.
- **Sitemap**: la lista de URLs que damos a Google. Ya lo enviamos en S08. Yoast lo mantiene solo.

---

## Canonical y datos estructurados

- **Canonical**: cuando un contenido vive en varias URLs, le dice a Google cuál es la buena. Yoast la pone sola; la vemos en `Ver código fuente`, buscando `rel="canonical"`.
- **Datos estructurados (Schema)**: le dicen a Google qué es cada cosa (artículo, producto, negocio). Permiten resultados enriquecidos. Yoast añade los básicos; lo comprobamos con el **Rich Results Test**.

---

## Al finalizar conseguiremos

- El sitio por encima de 75 en PageSpeed móvil.
- Caché activada y las imágenes comprimidas en WebP.
- Saber qué hacen robots.txt y el sitemap, y haberlos comprobado.
- Entender el canonical y los datos estructurados.

---

## Para la próxima

- Dejamos el sitio por encima de 75 en PageSpeed móvil.
- Comprobamos en casa el robots.txt y el canonical de la Landing.
- Traemos una lista de 10-15 palabras o frases por las que querríamos aparecer en Google.

La próxima: **keyword research, contenido y GEO**. Cierre del Módulo 1.

---

## Enlaces

- PageSpeed Insights: pagespeed.web.dev
- Core Web Vitals: web.dev/articles/vitals
- Rich Results Test: search.google.com/test/rich-results
- Schema.org: schema.org
