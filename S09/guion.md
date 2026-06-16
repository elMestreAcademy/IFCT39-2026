# S09 -- Medición: GA4 + Search Console

> Ayer (S08) todos salieron con: sitio dado de alta en Search Console, sitemap enviado, indexación solicitada, landing + 1 página nueva con on-page enlazadas, y un retoque de CSS.
> Hoy montamos la **analítica** (GA4 vía Site Kit) y aprendemos a **leer** las dos herramientas de medición. Search Console todavía tiene pocos datos (los sitemaps se enviaron ayer); leemos lo que ya hay y dejamos la lectura a fondo de queries para una sesión posterior, cuando haya semanas de datos.
> El **banner de cookies / RGPD NO es de hoy**: va a su propia sesión (la siguiente). Hoy GA4 queda recogiendo datos; en la sesión de normativa lo dejamos conforme.
> Sesión de 4 h (calendario real: 25 sesiones de 4 h). Esta es la sesión 13.

---

## Objetivos del día

1. **GA4 instalado y recogiendo datos** vía Site Kit, sin tocar código.
2. Saber **leer los informes básicos de GA4**: tiempo real, adquisición, páginas y eventos.
3. Entender **Search Console como fuente de verdad** y leer lo que ya hay: sitemap procesado, Indexación > Páginas, y dónde estarán las queries cuando lleguen.
4. Distinguir y combinar las **dos preguntas** de la medición: GA4 = qué hacen dentro de mi sitio; Search Console = cómo llegan a mi sitio desde Google.
5. Dejar el **panel de Site Kit** en el escritorio de WordPress como cuadro de mando unificado.

---

## Cronograma

| Tramo     | Min | Bloque                                                          |
| --------- | --- | --------------------------------------------------------------- |
| 0:00-0:20 | 20  | Apertura: checkpoint S08 (indexación, landing, página nueva)    |
| 0:20-0:50 | 30  | Las dos preguntas de la medición (teoría + tabla)               |
| 0:50-1:40 | 50  | GA4 con Site Kit: instalar y conectar (hands-on)                |
| 1:40-1:50 | 10  | Descanso                                                        |
| 1:50-2:40 | 50  | Leer GA4: tiempo real, adquisición, páginas, eventos            |
| 2:40-2:50 | 10  | Descanso                                                        |
| 2:50-3:40 | 50  | Search Console: leer lo que ya hay + conectarlo a Site Kit      |
| 3:40-4:00 | 20  | Cierre, deberes y conexión con la sesión de normativa           |

---

## Apertura: checkpoint S08

Cada uno verifica en su WP mientras paso lista de estado:

1. **Search Console**: en `Sitemaps`, el `sitemap_index.xml` aparece como "Correcto"? En `Indexación > Páginas`, sale ya algo? (deber de S08). Ronda rápida en voz alta.
2. **Landing terminada** (header, footer, hero) y la **página nueva** (Servicios o Sobre mí) publicada con su on-page. Quien no la acabara, es lo primero del día en paralelo.
3. **Sesión iniciada en su cuenta de Google**, la misma que usaron para Search Console: hoy la reutilizamos para GA4 (que sea dueño de su propia analítica).

Casos especiales: Ricardo (hosting propio) y Carlos (WP propio) ya verificaron con dominio propio; para GA4 no cambia nada respecto al resto.

---

## Las dos preguntas de la medición

El modelo mental que hay que llevarse de hoy: hay **dos herramientas** y cada una responde a **una pregunta distinta**.

- **Search Console (Google) = cómo me encuentra la gente.** Es lo que pasa ANTES de la visita: con qué búsquedas aparezco (queries), cuántas impresiones y clics tengo, en qué posición media salgo, qué páginas tiene indexadas Google. El dato lo pone Google. Es SEO puro.
- **GA4 / Analytics = qué hace la gente una vez dentro.** Es lo que pasa DESPUÉS del clic: cuántas visitas, de qué canal vienen, qué páginas ven, cuánto se quedan, qué acciones disparan. El dato lo pone el código que Site Kit mete en mi web.

| Pregunta            | Search Console            | GA4                                   |
| ------------------- | ------------------------- | ------------------------------------- |
| Responde a          | Cómo llegan a mí          | Qué hacen dentro                      |
| Momento             | Antes del clic            | Después del clic                      |
| Mide                | Impresiones, clics, posición, queries | Usuarios, sesiones, páginas, eventos |
| Fuente del dato     | Google                    | Snippet en tu web                     |
| Coste               | Gratis                    | Gratis                                |

**Por qué necesito las dos**: una sin la otra es media foto. Search Console me dice que aparezco para "fontanero madrid", pero no si esa visita hizo algo en mi web. GA4 me dice que una visita estuvo 3 minutos y rellenó el formulario, pero no con qué búsqueda llegó. Juntas cierran el círculo. Y Site Kit las enseña en el mismo panel.

**Aviso de expectativas** (decirlo claro y repetirlo): hoy los números van a ser casi cero. El sitio nació ayer y el único tráfico somos nosotros. Lo que se aprende hoy es DÓNDE mirar y QUÉ significa cada métrica, no a sacar conclusiones de negocio. Eso necesita semanas de datos.

---

## GA4 con Site Kit

Quienes hicieron el stretch de GA4 en S07 ya conocen Site Kit; hoy lo montamos todos. Seguimos el guion interno `stats-GA4.md`.

### Instalar y conectar

1. `Plugins > Añadir nuevo > "Site Kit by Google" > Instalar > Activar`.
2. Asistente de Site Kit: **"Iniciar configuración"** y login con la **misma cuenta de Google** que usaron para Search Console. Como ya verificaron Search Console ayer, Site Kit la detecta y la conecta sola (buen refuerzo de lo de S08).
3. Conceder los permisos que pide. Site Kit conecta primero Search Console.
4. Activar **Analytics** dentro de Site Kit: `Site Kit > Configuración > conectar Google Analytics`. Crear una **propiedad GA4 nueva**:
   - Cuenta de Analytics (crear una si no la tienen): nombre libre.
   - Propiedad: el nombre del sitio.
   - **Zona horaria: España (GMT+1). Moneda: EUR.**
   - Flujo de datos web: la URL del sitio (la rellena Site Kit).
5. Site Kit inserta el snippet de GA4 en **todas las páginas** automáticamente, sin tocar código.

### Comprobar que mide

Abrir el sitio en una pestaña de **incógnito** y, en GA4 > Informes > **Tiempo real**, verse a uno mismo como usuario activo. Si aparece, GA4 está funcionando.

### Nota de orden y RGPD (decirlo en voz alta)

Lo correcto por ley es que el **banner de cookies vaya ANTES** de que cargue GA4 (consentimiento previo). Hoy instalamos GA4 sin banner todavía por dos razones: (a) GA4 necesita tiempo recogiendo datos antes de poder leerlo con sentido, y (b) son sitios de prácticas, sin tráfico real. En la **sesión de normativa** (la siguiente) montamos el banner con Complianz y activamos el **modo de consentimiento de Google**, que bloquea GA4 hasta que el visitante acepta. Queda apuntado como deuda hasta entonces. No es un detalle: es el motivo por el que la normativa va pegada a la medición.

---

## Leer GA4

Dos sitios donde se lee:

- **Dentro de WordPress**: `Escritorio > Site Kit`, resumen rápido (lo justo para no salir de WP).
- **En GA4 completo**: `analytics.google.com` con su cuenta. Aquí está todo.

Recorrido (proyectar y que repliquen en su pantalla):

- **Tiempo real**: usuarios activos ahora mismo. Ejercicio: que cada uno abra el sitio del compañero de al lado y se vean aparecer en directo. Inmediato y motivador.
- **Informes > Adquisición > Adquisición de tráfico**: los **canales** (Organic Search, Direct, Referral, Social). Explicar qué es cada uno y por qué ahora casi todo cae en "Direct": entran escribiendo la URL o desde un marcador, no desde una búsqueda.
- **Informes > Interacción > Páginas y pantallas**: qué páginas se ven más.
- **Medición mejorada (eventos automáticos)**: GA4 ya mide solo `page_view`, scroll, clics salientes, etc. No hay que configurar nada para lo básico.

Vocabulario mínimo de GA4 (en pantalla):

| Término                     | Qué es                                                        |
| --------------------------- | ------------------------------------------------------------ |
| Usuario                     | Persona única (por dispositivo / navegador)                  |
| Sesión                      | Una visita; se corta tras 30 min de inactividad              |
| Evento                      | Cualquier acción medida: `page_view`, scroll, clic, descarga |
| Sesión con interacción      | Sesión de más de 10 s, o con 2+ páginas, o con conversión    |
| Evento clave (conversión)   | El evento que te importa: enviar formulario, comprar         |

Idea de fondo: **GA4 es un modelo de eventos** (todo es un evento), a diferencia del viejo Universal Analytics que giraba en torno a páginas y sesiones. Mención breve, no hace falta más.

Repetir el aviso: los números de hoy son de juguete. El objetivo es saber moverse por la interfaz.

---

## Search Console: leer lo que ya hay

Volvemos a la herramienta de ayer, ahora a **leerla** (ayer solo la dimos de alta).

1. **El sitemap se procesó?** `Sitemaps`: estado "Correcto" y número de páginas descubiertas. Si sigue "No se ha podido obtener", revisar que la URL sea `sitemap_index.xml` exacta.
2. **Indexación > Páginas**: cuántas indexadas frente a no indexadas, y por qué. Motivos normales en un sitio nuevo: "Rastreada: actualmente sin indexar" o "Descubierta: no indexada" significan **paciencia**, no error. Esto sí tiene algo que mirar hoy.
3. **Inspección de URL**: pegar la landing en la barra superior. Estado de indexación, "Probar URL publicada", y "Solicitar indexación" si aún no está.
4. **Rendimiento**: aquí viven queries, impresiones, clics y posición media. AVISO: en un sitio de días suele estar casi vacío. Lo abrimos solo para **conocer la pantalla** (los 4 cuadros de arriba y las pestañas Consultas / Páginas / Países / Dispositivos). La **lectura a fondo de queries la dejamos para una sesión posterior**, cuando haya 3-4 semanas de datos. Apuntarlo: "volveremos aquí con datos reales".
5. **Search Console dentro de Site Kit**: como se conectó en la instalación, ya aparece en el escritorio de WP. Así ven Search Console y GA4 en el **mismo cuadro de mando** sin salir de WordPress. Ese es el premio de hoy: un panel único.

---

## Cierre

### Qué tienen hoy

- GA4 instalado vía Site Kit, recogiendo datos desde ahora.
- Saben leer los informes básicos de GA4: tiempo real, adquisición, páginas.
- Saben leer el estado de indexación y el sitemap en Search Console, y dónde estarán las queries cuando lleguen.
- Site Kit como panel único (Search + Analytics) en el escritorio de WP.

### Deberes para la próxima

1. **Generar algo de tráfico real**: compartir la URL del sitio con 2-3 conocidos y pedirles que entren y naveguen. La próxima sesión habrá datos de verdad en Tiempo real y Adquisición.
2. Entrar a GA4 desde casa una vez y mirar **Tiempo real**: se registró la visita de esos conocidos?
3. (Del sitio) Tener pensado o redactado el contenido de la página de **Contacto**: en la sesión de normativa publicamos también el aviso legal y la política de privacidad, y conviene dejar el footer legal listo.

### Próxima sesión: Normativa y cookies

El sitio ya **mide**, pero todavía **no es legal**: falta el banner de cookies y la política de privacidad. La próxima sesión montamos el banner con **Complianz**, publicamos la **política de privacidad** (WordPress ya la trae como borrador) y activamos el **modo de consentimiento** para que GA4 solo cargue tras la aceptación. Es ley, no es opcional.

---

## Recursos

- [Site Kit by Google](https://sitekit.withgoogle.com/)
- [Google Analytics (GA4)](https://analytics.google.com/)
- [Ayuda de GA4 (Google)](https://support.google.com/analytics/answer/9304153)
- [Google Search Console](https://search.google.com/search-console)
- Interno: `stats-GA4.md`
