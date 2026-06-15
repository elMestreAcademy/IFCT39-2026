# S07 -- SEO on-page formalizado + Search Console (+ GA4 si llegamos)

> Ayer (S06) todos salieron con: Yoast activo, permalinks bien, 1 página (landing) + 1 entrada publicadas y el snippet editado.
> La configuración de Yoast ya tocó de pasada contenidos de S08; hoy se formalizan.
> Esta sesión absorbe la teoría on-page de S08 y adelanta GA4 de S09 si da tiempo.
> CAMBIO DE ENFOQUE desde hoy: el proyecto es un **sitio estático tipo negocio** (páginas como núcleo). El blog y las entradas quedan como opcional para quien tenga proyecto de contenido.

---

## Objetivos del día

1. **Formalizar el SEO on-page**: que entiendan POR QUÉ ayer rellenaron los campos de Yoast (title, meta, slug, H1-H3, enlazado interno).
2. **Sitio verificado en Search Console** con sitemap enviado e indexación solicitada.
3. Entender **qué es Gutenberg** y qué cambia con un tema de bloques (Twenty Twenty-Five).
4. **Sitio estático tipo negocio**: landing con barra de navegación superior, footer adaptado y esqueleto de páginas (Inicio, Servicios, Sobre mí, Contacto), vía editor del sitio.
5. *(Stretch)* GA4 instalado vía Site Kit.

---

## Cronograma

| Tramo     | Min | Bloque                                                          |
| --------- | --- | --------------------------------------------------------------- |
| 0:00-0:15 | 15  | Apertura: checkpoint S06 + repaso de deberes (3 títulos)        |
| 0:15-0:45 | 30  | Qué es Gutenberg y el editor del sitio (teoría con demo)        |
| 0:45-1:30 | 45  | SEO on-page formalizado: la chuleta + aplicarla a sus 2 URLs    |
| 1:30-1:40 | 10  | Descanso                                                        |
| 1:40-2:30 | 50  | Search Console: propiedad, verificación, sitemap, indexación    |
| 2:30-2:40 | 10  | Descanso                                                        |
| 2:40-4:00 | 80  | Landing con Twenty Twenty-Five: header + footer + patrones      |
| 4:00-4:45 | 45  | GA4 con Site Kit (solo si vamos bien; si no, más landing)       |
| 4:45-5:00 | 15  | Cierre, deberes y conexión con S08                              |

---

## Apertura: checkpoint

Cada uno verifica en su WP mientras paso lista de estado:

1. Entrada de S06 **publicada** (no borrador) y con "Frase clave" rellena en Yoast.
2. **3 títulos** pensados como búsquedas reales (deber de S06). Ronda rápida en voz alta: el grupo dice si "eso lo busca alguien".
3. **Sesión iniciada en la cuenta de Google** que usarán para Search Console (deber 2 de S06). Quien no la tenga, la crea ahora en paralelo.

---

## Qué es Gutenberg 

### El concepto

- **Gutenberg es el editor de bloques de WordPress**, el editor por defecto desde WP 5.0 (2018).
- Antes existía el "editor clásico": una caja de texto tipo Word y el tema mandaba sobre todo lo demás. Con Gutenberg, **todo es un bloque**: párrafo, título, imagen, botón, columnas, vídeo. Cada bloque se inserta, se mueve y se configura por separado.
- Ya lo llevan usando dos sesiones sin saberlo: el editor donde escribieron su entrada ES Gutenberg.

### Vocabulario (en pantalla, señalando cada cosa)

| Término             | Qué es                                                                |
| ------------------- | -------------------------------------------------------------------   |
| Bloque              | Unidad mínima: un párrafo, una imagen, un botón                       |
| Patrón              | Composición prefabricada de bloques (un hero, una rejilla de precios) |
| Parte de plantilla  | Bloques compartidos por todo el sitio: header, footer                 |
| Plantilla           | Esqueleto de un tipo de página: página, entrada, archivo, 404         |
| Editor del sitio    | `Apariencia > Editor`: donde se editan plantillas y partes            |

### Por qué nos importa hoy

**Twenty Twenty-Five es un tema de bloques**: no tiene el personalizador clásico ni `Apariencia > Menús`. El header, el footer y los menús se editan con bloques en el editor del sitio. Es decir: la misma herramienta que ya conocen del contenido sirve ahora para la estructura. Eso es Full Site Editing.

Trucos de manejo para la demo:

- Teclear `/` en una línea vacía abre el insertador de bloques.
- El icono de **vista de lista** (tres rayas, arriba a la izquierda) muestra el árbol de bloques: imprescindible para no perderse.
- Cada bloque tiene su barra de herramientas flotante + panel lateral de ajustes.
---

## SEO on-page formalizado

### Resumen

| Elemento          | Regla                                                                     | Dónde se toca             |
| ----------------- | ------------------------------------------------------------------------- | ------------------------- |
| SEO title         | 50-60 caracteres, keyword al principio, marca al final                    | Panel Yoast               |
| Meta description  | 120-155 caracteres, keyword + invitación al clic                          | Panel Yoast               |
| Slug              | Corto, con keyword, sin preposiciones ni fechas                           | Panel Yoast / permalink   |
| H1                | Uno solo por página = el título del post                                  | Título en el editor       |
| H2 / H3           | Jerarquía real: H2 secciones, H3 subsecciones, con variaciones de keyword | Bloques de título         |
| Primer párrafo    | La keyword aparece en las primeras 100 palabras                           | Contenido                 |
| Imágenes          | Atributo alt descriptivo (accesibilidad + Google Imágenes)                | Ajustes del bloque imagen |
| Enlazado interno  | Cada pieza enlaza al menos a otra del propio sitio                        | Contenido                 |

**Yoast no hace SEO, lo chequea**. El semáforo verde solo confirma que has hecho tú el trabajo de esta tabla.

### Ejercicio: pasar la chuleta a sus 2 URLs

Cada uno revisa su landing y su entrada contra la tabla, fila por fila. Obligatorio:

1. Corregir lo que falle (alts vacíos y jerarquía de títulos serán lo más común).
2. Añadir **un enlace interno en cada dirección**: la entrada enlaza a la landing y la landing a la entrada (texto de ancla descriptivo, no "pincha aquí").

Rotar por mesas. Con esto cumplen el hito "on-page optimizado en al menos 2 URLs" que estaba previsto para S08.

---

## Search Console

### Qué es

La herramienta donde Google te cuenta cómo te ve: con qué búsquedas apareces (queries), cuántas impresiones y clics tienes, qué páginas tiene indexadas y qué errores encuentra. Es gratuita y es LA fuente de verdad del SEO; todo lo demás son estimaciones.

Callback a S04: aquel registro TXT de DNS que dejamos pendiente era para esto.

### Crear la propiedad

En [search.google.com/search-console](https://search.google.com/search-console) con su cuenta de Google:

- Tipo **"Prefijo de URL"** con `https://wpN.masterfactories.com` exacto (con https y sin barra extra).
- NO usar el tipo "Dominio": pide verificación por DNS y ellos no controlan el DNS de masterfactories.com.
- **Excepción Ricardo** (hosting propio): él sí puede crear propiedad de Dominio y verificar con el registro TXT. Si hay tiempo, hacerlo en pantalla como demo del callback de S04.

### Verificar con Yoast

Método "Etiqueta HTML" sin tocar código:

1. En Search Console, elegir verificación por **etiqueta HTML** y copiar solo el valor de `content="..."`.
2. En WP: `Yoast SEO > Ajustes > Conexiones del sitio` (en versiones antiguas: Herramientas para webmasters) > pegar en el campo de Google > Guardar.
3. Volver a Search Console > **Verificar**.

Si alguien se atasca, el plan B es Site Kit (que verifica solo), pero mejor que vean el mecanismo de la etiqueta primero.

### Sitemap + indexación

1. Abrir `https://wpN.masterfactories.com/sitemap_index.xml` en el navegador: ese fichero lo genera Yoast y es el índice de todo lo publicado.
2. En Search Console: `Sitemaps > Añadir sitemap > sitemap_index.xml > Enviar`.
3. **Inspección de URL**: pegar la URL de la landing en la barra superior > "Solicitar indexación". Repetir con la entrada.

Gestionar expectativas: la indexación tarda días y los primeros datos de queries, semanas. Hoy plantamos; los informes los leeremos en S08 y siguientes.



---

## Landing con Twenty Twenty-Five

### Fase 1 -- Página de inicio estática

`Ajustes > Lectura > Una página estática > seleccionar su landing como "Página de inicio"`.
Así su landing responde en la raíz del dominio (mejor para SEO y para Search Console).

### Fase 2 -- Barra de navegación superior

1. `Apariencia > Editor > Patrones > Partes de plantilla > Cabecera` (header).
2. Localizar el bloque **Navegación** en la vista de lista (si el header de TT25 no lo trae, insertarlo junto al título del sitio).
3. Añadir enlaces a sus páginas: Inicio, Servicios, Sobre mí, Contacto (las que no existan, crearlas como borrador desde el propio bloque). El enlace a Blog, solo quien lo mantenga.
4. **Guardar**: avisar de que el header es parte de plantilla y el cambio afecta a TODO el sitio.
5. Extra para los rápidos: seleccionar el grupo que envuelve el header y en ajustes de posición ponerlo **fijo (sticky)** para que la barra acompañe al hacer scroll.

### Fase 3 -- Footer

1. `Apariencia > Editor > Patrones > Partes de plantilla > Pie de página` (footer).
2. Quitar o reescribir los créditos por defecto ("Diseñado con WordPress").
3. Dejar un footer mínimo digno: nombre del sitio + tagline, bloque **Iconos sociales** con sus redes reales, y un segundo bloque Navegación con enlaces secundarios (aviso legal y privacidad cuando existan, en S09 con el GDPR).

### Fase 4 -- Cuerpo de la landing con patrones

Editar la página de la landing y componerla con patrones de TT25 (insertador > pestaña Patrones):

- **Hero** arriba: bloque Cubierta (imagen de fondo + H1 + botón CTA) o un patrón de la categoría correspondiente.
- Una sección de **columnas** (3 servicios / 3 razones / 3 productos).
- Un **CTA final** con botón.

Recordar la chuleta on-page de la mañana: el H1 del hero lleva la keyword; los títulos de sección son H2.

---

## GA4 con Site Kit -- SOLO si vamos bien de tiempo

Seguir el guion de `stats-GA4.md`. Resumen:

1. `Plugins > Añadir nuevo > "Site Kit by Google" > Instalar > Activar`.
2. Asistente de Site Kit: login con la misma cuenta de Google de Search Console. Detectará la propiedad ya verificada (refuerzo de lo hecho hoy).
3. Activar Analytics dentro de Site Kit: crear propiedad GA4 nueva (zona horaria España, moneda EUR). Site Kit inserta el snippet en todas las páginas sin tocar código.
4. Aviso legal: **falta el banner de cookies (GDPR)** para estar en regla. Lo montamos en S09 con Complianz; no es opcional, es ley.

Si no llegamos: no pasa nada, era material de S09. El tiempo se queda en la landing.

---

## RESERVA: editar CSS -- sin hueco en el cronograma, tenerlo a mano

Material previsto para S08, pero si la landing va fina y alguien pide "cambiar el aspecto", esto es lo que se enseña. De menos a más CSS:

### 1. Estilos globales (cero CSS)

`Apariencia > Editor > Estilos` (icono del círculo bicolor): paleta de colores, tipografías y espaciados de todo el sitio desde la interfaz. TT25 trae **variaciones de estilo** completas: un clic y el sitio cambia de personalidad. Para perfiles no técnicos esto ya es "aplicar diseño".

### 2. CSS adicional global

`Apariencia > Editor > Estilos > menú de tres puntos > CSS adicional`. Caja de CSS con vista previa en vivo, se aplica a todo el sitio. Aviso: va ligado al tema activo; si cambian de tema no viaja.

### 3. Clase propia + CSS (recicla S05)

1. Seleccionar un bloque (p. ej. su botón CTA) > panel lateral > `Avanzado > Clases CSS adicionales` > escribir `boton-cta`.
2. En CSS adicional:

```css
.boton-cta a {
    background-color: #c0392b;
    border-radius: 8px;
    padding: 12px 28px;
}

.boton-cta a:hover {
    background-color: #e74c3c;
}
```

Es exactamente lo de S05 (selectores, clases, hover) pero sobre su web real.

Tip DevTools (callback S03): todos los bloques tienen clases predecibles (`.wp-block-button`, `.wp-block-cover`, `.wp-block-heading`); se pueden estilar sin añadir clases propias.

Regla de orden para que no se peleen con el tema: **primero la interfaz, luego el CSS**. Color, tipografía o espaciado de un bloque se hacen desde el panel del bloque; el CSS adicional es para lo que la interfaz no alcanza (hovers, sombras, detalles finos).

---

## Cierre

### Qué tienen hoy

- On-page formalizado en 2 URLs (hito de S08 cumplido).
- Sitio verificado en Search Console, sitemap enviado, indexación solicitada (hito de S07 cumplido).
- Landing con barra de navegación, footer propio y estructura por patrones.
- (Si hubo tiempo) GA4 recogiendo datos desde hoy.

### Deberes para S08

1. Terminar la landing quien no la acabara (header + footer + hero como mínimo).
2. Redactar y publicar **una página nueva del sitio** (Servicios o Sobre mí), pasándole la chuleta on-page completa antes de publicar. *(Opcional, perfiles blog)*: además o en su lugar, una entrada con uno de los 3 títulos de hoy.
3. Entrar a Search Console desde casa y mirar `Indexación > Páginas`: ¿aparece ya algo? Traer la respuesta.

### S08

Con la teoría on-page ya dada, S08 pasa a ser **taller**: completar el esqueleto de páginas del sitio de negocio, optimización fina sobre sus URLs, primeras lecturas de Search Console (cobertura, queries si las hay) y enlazado interno entre páginas. Además, **CSS sobre su sitio real**: `Apariencia > Editor > Estilos > CSS adicional` + clases propias por bloque (`Avanzado > Clases CSS adicionales`), reciclando el CSS de S05. Colchón para rematar lo que hoy se quede a medias.

---

## Recursos

- [Google Search Console](https://search.google.com/search-console)
- [Conectar tu web a Search Console con Yoast](https://yoast.com/help/how-to-connect-your-website-to-google-search-console/)
- [El editor del sitio (WordPress.org)](https://wordpress.org/documentation/article/site-editor/)
- [Bloque de navegación (WordPress.org)](https://wordpress.org/documentation/article/navigation-block/)
- [Tema Twenty Twenty-Five](https://wordpress.org/themes/twentytwentyfive/)
- [Biblioteca de patrones de WordPress](https://wordpress.org/patterns/)
- [Site Kit by Google](https://sitekit.withgoogle.com/)


### Nota: Guarar patrón

1. Patrones sincronizados (Synced Patterns) — lo que antes se llamaba "bloques reutilizables" (renombrado en WP 6.3). Seleccionas el bloque o grupo de bloques → menú de opciones (⋮) → "Crear patrón" → activas el toggle de sincronizado. A partir de ahí lo insertas en cualquier página/entrada desde el insertador (pestaña Patrones). La clave: si lo editas en un sitio, cambia en todos los lugares donde está insertado. Es una referencia, no una copia.

2. Patrones no sincronizados — mismo flujo pero sin el toggle. Al insertarlo crea una copia independiente: plantilla de partida, no instancia compartida. Útil para estructuras que repites pero personalizas (tarjetas de servicio, CTAs por landing).

Para cabeceras específicamente: si estás en un tema de bloques (que es lo que recomendabas para el curso), la cabecera no es un patrón sino una template part (parte de plantilla). Se edita en Apariencia → Editor → Partes de plantilla. Por naturaleza ya es global: la tocas una vez y se propaga a todas las plantillas que la usan. Puedes tener varias (header por defecto, header minimal para landings) y asignarlas por plantilla.
Detalle útil para clase: dentro de una template part puedes insertar patrones sincronizados, así que se pueden componer. Y los patrones se gestionan centralizadamente en Apariencia → Editor → Patrones (o /wp-admin/site-editor.php?path=/patterns), donde puedes renombrar, duplicar y desincronizar.
La distinción sincronizado/no sincronizado es exactamente el tipo de cosa que cae bien como ejercicio práctico en IFCT39: que creen un CTA sincronizado, lo metan en tres páginas, lo editen una vez y vean la propagación.