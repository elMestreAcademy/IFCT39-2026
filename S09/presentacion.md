---
marp: true
paginate: true
---

# Medición: GA4 y Search Console

Sesión S09

---

## Hoy

Instalamos la analítica del sitio y aprendemos a leer las dos herramientas de medición. Al finalizar conseguiremos:

- GA4 instalado y recogiendo datos, vía Site Kit y sin tocar código.
- Saber leer los informes básicos de GA4: tiempo real, adquisición, páginas.
- Saber leer Search Console: sitemap, indexación y dónde aparecerán las búsquedas.
- Site Kit como panel único de medición en el escritorio de WordPress.

---

## Requisitos de sesiones anteriores

- El sitio dado de alta en Search Console, con el sitemap enviado (S08).
- La Landing y una página nueva publicadas, con su on-page.
- La cuenta de Google lista: la misma que usamos para Search Console.

Si falta algo, eso es lo primero de hoy.

---

## Las dos preguntas de la medición

Hay dos herramientas y cada una responde a una pregunta distinta:

- **Search Console**: cómo nos encuentra la gente. Lo que pasa **antes** de la visita.
- **GA4 / Analytics**: qué hace la gente una vez dentro. Lo que pasa **después** del clic.

Una sin la otra es media foto. Juntas cierran el círculo, y Site Kit las enseña en el mismo panel.

---

## Search Console y GA4, comparadas

| Pregunta        | Search Console               | GA4                                  |
| --------------- | ---------------------------- | ------------------------------------ |
| Responde a      | Cómo llegan a mí             | Qué hacen dentro                     |
| Momento         | Antes del clic               | Después del clic                     |
| Mide            | Impresiones, clics, posición | Usuarios, sesiones, páginas, eventos |
| Fuente del dato | Google                       | El código en nuestra web             |
| Coste           | Gratis                       | Gratis                               |

---

## Expectativas de hoy

Los números van a ser casi cero: el sitio nació ayer y el único tráfico somos nosotros.

Lo que aprendemos hoy es **dónde mirar** y **qué significa** cada métrica, no a sacar conclusiones de negocio. Eso necesita semanas de datos.

---

## GA4 con Site Kit: instalar y conectar

1. `Plugins > Añadir nuevo > "Site Kit by Google" > Instalar > Activar`.
2. Asistente de Site Kit: login con la **misma cuenta de Google** de Search Console. La detecta y la conecta sola.
3. Conceder los permisos. Site Kit conecta primero Search Console.
4. Activar **Analytics** y crear una **propiedad GA4 nueva**: zona horaria España, moneda EUR.
5. Site Kit inserta el código de GA4 en todas las páginas, sin tocar nada.

---

## Comprobar que mide

Abrimos el sitio en una pestaña de **incógnito** y vamos a GA4 > Informes > **Tiempo real**.

Si nos vemos como usuario activo, GA4 está funcionando.

---

## Orden y cookies (RGPD)

Por ley, el banner de cookies debe cargar **antes** que GA4 (consentimiento previo).

Hoy instalamos GA4 sin banner todavía, por dos razones:

- GA4 necesita tiempo recogiendo datos antes de poder leerlo.
- Son sitios de prácticas, sin tráfico real.

En la **próxima sesión** montamos el banner y activamos el consentimiento para que GA4 solo cargue tras la aceptación.

---

## Leer GA4: dónde se lee

Dos sitios:

- Dentro de WordPress: `Escritorio > Site Kit`, resumen rápido.
- En GA4 completo: `analytics.google.com`. Aquí está todo.

---

## Leer GA4: el recorrido

- **Tiempo real**: usuarios activos ahora mismo. Abrimos el sitio del compañero y nos vemos aparecer.
- **Adquisición > Adquisición de tráfico**: los canales (Organic Search, Direct, Referral, Social). Ahora casi todo es "Direct".
- **Interacción > Páginas y pantallas**: qué páginas se ven más.
- **Medición mejorada**: GA4 ya mide solo páginas vistas, scroll y clics, sin configurar nada.

---

## Vocabulario de GA4

| Término                   | Qué es                                              |
| ------------------------- | --------------------------------------------------- |
| Usuario                   | Persona única, por dispositivo o navegador          |
| Sesión                    | Una visita; se corta tras 30 min de inactividad     |
| Evento                    | Cualquier acción medida: página vista, scroll, clic |
| Sesión con interacción    | Más de 10 s, o 2+ páginas, o una conversión         |
| Evento clave (conversión) | El que nos importa: enviar formulario, comprar      |

GA4 es un modelo de **eventos**: todo lo que se mide es un evento.

---

## Search Console: leer lo que ya hay

Volvemos a la herramienta de ayer, ahora para leerla.

- **Sitemaps**: estado "Correcto" y número de páginas descubiertas.
- **Indexación > Páginas**: indexadas frente a no indexadas. En un sitio nuevo, "sin indexar todavía" significa paciencia, no error.
- **Inspección de URL**: pegamos la Landing, vemos su estado y solicitamos indexación si hace falta.

---

## Search Console: las búsquedas, más adelante

En **Rendimiento** viven las búsquedas, impresiones, clics y posición media.

En un sitio de días está casi vacío. Hoy solo conocemos la pantalla; lo leeremos a fondo en una sesión posterior, cuando haya semanas de datos.

---

## El premio: un panel único

Search Console y GA4 quedan conectados dentro de **Site Kit**.

Así vemos las dos herramientas en el mismo cuadro de mando, en el escritorio de WordPress, sin salir del sitio.

---

## Al finalizar conseguiremos

- GA4 instalado y recogiendo datos desde ahora.
- Saber leer los informes básicos de GA4.
- Saber leer el estado de indexación y el sitemap en Search Console.
- Site Kit como panel único de medición.

---

## Para la próxima

- Compartimos la URL del sitio con 2-3 conocidos y les pedimos que entren y naveguen: así habrá datos de verdad.
- Entramos a GA4 desde casa y miramos Tiempo real.
- Dejamos pensado el contenido de la página de **Contacto**.

Y montamos la **normativa**: banner de cookies y política de privacidad. Es ley, no es opcional.

---

## Enlaces

- Site Kit by Google: sitekit.withgoogle.com
- Google Analytics: analytics.google.com
- Google Search Console: search.google.com/search-console
