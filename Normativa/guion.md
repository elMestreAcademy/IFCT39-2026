# Normativa -- Cookies, RGPD y consentimiento

> Ayer (S09) montamos la analítica: GA4 quedó recogiendo datos vía Site Kit y aprendimos a leer GA4 y Search Console. Quedó una deuda apuntada en voz alta: el sitio **mide pero todavía no es legal**, porque GA4 carga sin pedir permiso.
> Hoy la saldamos. Montamos el **banner de cookies** con Complianz, publicamos las **páginas legales** (privacidad, cookies, aviso legal) y activamos el **modo de consentimiento** para que GA4 solo cargue cuando el visitante acepta. Esto no es opcional: es ley (RGPD + LSSI).
> Sesión de 4 h (calendario real: 25 sesiones de 4 h). Esta es la sesión 14.

---

## Objetivos del día

1. Entender **por qué es obligatorio**: RGPD y LSSI-CE, y qué pasa si no se cumple.
2. Saber qué **tres documentos legales** necesita un sitio y para qué sirve cada uno.
3. Montar el **banner de cookies** con Complianz: aceptar, rechazar y preferencias.
4. Publicar la **política de privacidad, la de cookies y el aviso legal**, y enlazarlas en el footer.
5. Activar el **modo de consentimiento de Google** para que GA4 no cargue hasta que el visitante acepta, y comprobar que funciona.

---

## Cronograma

| Tramo     | Min | Bloque                                                          |
| --------- | --- | --------------------------------------------------------------- |
| 0:00-0:20 | 20  | Apertura: checkpoint S09 (GA4 mide, tráfico de los deberes)     |
| 0:20-1:00 | 40  | Por qué la ley: RGPD y LSSI, los tres documentos                |
| 1:00-1:50 | 50  | Complianz: instalar y configurar el banner (hands-on)           |
| 1:50-2:00 | 10  | Descanso                                                        |
| 2:00-2:40 | 40  | Páginas legales: privacidad, cookies y aviso legal              |
| 2:40-2:50 | 10  | Descanso                                                        |
| 2:50-3:30 | 40  | Modo de consentimiento sobre GA4 + comprobar                    |
| 3:30-4:00 | 30  | Footer legal, cierre, deberes y conexión con S10                |

---

## Apertura: checkpoint S09

Cada uno verifica en su WP mientras paso lista de estado:

1. **GA4 está midiendo?** En `Escritorio > Site Kit` o en `analytics.google.com > Tiempo real`, sale algo. Quien no terminara la instalación de ayer, es lo primero del día en paralelo.
2. **Tráfico de los deberes**: pidieron a 2-3 conocidos que entraran? Miramos en GA4 > Adquisición si ha caído alguna visita nueva (ya no solo "Direct" nuestro).
3. **Página de Contacto**: traen pensado o redactado el contenido? Hoy publicamos el footer legal y conviene rematar Contacto en la misma pasada.

Casos especiales: Ricardo (hosting propio) y Carlos (WP propio) tienen dominio propio y datos reales para el aviso legal; el resto pueden usar datos de ejemplo coherentes, pero entendiendo qué va en cada hueco.

---

## Por qué la ley

El modelo mental de hoy: un sitio que recoge datos (y GA4 los recoge) tiene **obligaciones legales**. No cumplirlas expone a sanciones reales de la AEPD.

Tres normas que nos afectan:

- **RGPD** (Reglamento europeo de protección de datos): regula el tratamiento de datos personales. Exige consentimiento **previo, informado, granular y revocable**.
- **LOPDGDD** (ley española que desarrolla el RGPD): lo aterriza en España.
- **LSSI-CE** (ley de servicios de la sociedad de la información): obliga al **aviso legal** y regula las **cookies**.

La regla práctica de las cookies:

- Las cookies **técnicas** (las que hacen funcionar el sitio) no necesitan permiso.
- Las de **analítica, publicidad o seguimiento** (GA4 entra aquí) necesitan **consentimiento previo**: no pueden cargar hasta que el visitante acepta.
- **Rechazar tiene que ser tan fácil como aceptar.** Nada de un botón gigante de "Aceptar" y un enlace escondido para rechazar. Eso es ilegal y la AEPD multa por ello.

Los **tres documentos legales** que vamos a dejar publicados:

| Documento               | Qué dice                                                        | De dónde sale                  |
| ----------------------- | --------------------------------------------------------------- | ------------------------------ |
| Aviso legal (LSSI)      | Quién es el titular: nombre, NIF, contacto, condiciones de uso  | Lo redactamos / plantilla      |
| Política de privacidad  | Qué datos recojo, para qué, base legal, derechos del usuario    | Borrador de WordPress + ajustes|
| Política de cookies     | Qué cookies hay, de quién, para qué y cuánto duran              | La genera Complianz            |

Idea de fondo: el banner es la **puerta**; las tres páginas son la **letra pequeña** a la que enlaza. Las dos cosas van juntas.

---

## Complianz: el banner

Hay varios plugins de cookies. Usamos **Complianz** porque genera el banner, las páginas legales y la señal de consentimiento de una sola pieza, y se lleva bien con Site Kit.

### Instalar y configurar

1. `Plugins > Añadir nuevo > "Complianz | GDPR/CCPA Cookie Consent" > Instalar > Activar`.
2. Arranca el **asistente de Complianz**. Lo recorremos juntos:
   - **Región**: solo **Europa** (es lo que nos aplica). Sin Estados Unidos ni otras.
   - **Servicios que usan cookies**: marcar que usamos **Google Analytics** (lo detecta por Site Kit / GA4).
   - **Tipo de consentimiento**: **Opt-in** (en Europa, permiso previo: nada carga hasta aceptar).
   - **Documentos**: dejar que Complianz **genere la política de cookies**, y enlazar la de privacidad.
3. **Escaneo de cookies**: Complianz rastrea el sitio y lista qué cookies pone (verán las de GA4). Esto alimenta la política de cookies sola.
4. **El banner**: tres opciones visibles y al mismo nivel: **Aceptar**, **Rechazar** y **Preferencias**. Repetir la regla: rechazar tan visible como aceptar.
5. **Publicar** y comprobar que el banner aparece.

### Comprobar

Abrir el sitio en una pestaña de **incógnito**: tiene que saltar el banner antes de poder navegar tranquilo. Si no aparece, revisar que Complianz esté activado y el banner publicado.

---

## Páginas legales

Ahora la letra pequeña a la que enlaza el banner.

1. **Política de cookies**: ya la generó Complianz en el paso anterior. Solo comprobar que existe como página publicada.
2. **Política de privacidad**: WordPress trae un **borrador** listo. En `Ajustes > Privacidad` se elige o se crea la página de privacidad; WordPress rellena una plantilla con los apartados típicos (qué datos, para qué, derechos). Hay que **revisarla y adaptarla**: mencionar a **Google (Analytics)** como encargado que trata datos por nosotros, y los **derechos** del usuario (acceso, rectificación, supresión, oposición).
3. **Aviso legal**: lo redactamos a partir de una plantilla. Datos del **titular**: nombre o razón social, NIF, domicilio o email de contacto, y la finalidad del sitio. Quien use datos de ejemplo, que sean coherentes (no dejar "XXXX").

Las tres quedan como páginas publicadas. Las enlazaremos en el footer al final.

---

## Modo de consentimiento sobre GA4

Aquí está el meollo legal: que GA4 **no cargue hasta que el visitante acepta**.

- **Google Consent Mode**: GA4 espera una señal de consentimiento antes de medir con cookies. Complianz envía esa señal según lo que pulse el visitante.
- Activarlo en `Complianz > Integraciones`: marcar **Google Consent Mode** (y que detecte Site Kit / GA4).
- Qué pasa entonces:
  - **Antes de aceptar**: GA4 no usa cookies ni identifica al visitante (modo denegado).
  - **Tras aceptar**: GA4 mide con normalidad, como ayer.

### Comprobar que funciona

1. Incógnito, abrir el sitio: salta el banner, GA4 en **Tiempo real** no debería contar la visita como antes (sin aceptar).
2. Pulsar **Aceptar**: recargar y volver a GA4 > Tiempo real. Ahora sí aparece la visita.
3. Repetir pulsando **Rechazar** en otra ventana incógnito: comprobar que respeta el "no".

Decirlo en voz alta: este es exactamente el motivo por el que ayer instalamos GA4 sin banner (necesitaba arrancar a recoger datos) y hoy lo dejamos conforme. La deuda queda saldada.

---

## Footer legal

Cierre práctico: dejar los tres enlaces siempre a la vista.

- En `Apariencia > Widgets` o en el editor del tema, añadir al **footer** un menú o lista con: **Aviso legal**, **Política de privacidad** y **Política de cookies**.
- Complianz suele añadir solo un enlace de "Gestionar consentimiento" para que el visitante pueda **cambiar de opinión**: comprobar que está (es un derecho, el consentimiento es revocable).

Si da tiempo, rematamos también la página de **Contacto** (deber de ayer) y la enlazamos.

---

## Cierre

### Qué tienen hoy

- Banner de cookies de Complianz funcionando, con aceptar y rechazar al mismo nivel.
- Las tres páginas legales publicadas: privacidad, cookies y aviso legal.
- GA4 bajo modo de consentimiento: solo mide tras la aceptación.
- Footer legal con los enlaces y la opción de revocar el consentimiento.

### Deberes para la próxima

1. **Probar el banner desde casa** en incógnito: aparece, y rechazar funciona de verdad?
2. **Rellenar los datos del aviso legal** con su identidad (o una ficticia coherente), sin huecos sin completar.
3. Para S10, no instalar plugins de más: **cada plugin pesa** y la próxima sesión va de **velocidad**. Mejor llegar con el sitio ligero.

### Próxima sesión: SEO técnico y velocidad

El sitio ya mide y ya es legal. La próxima miramos que sea **rápido y rastreable**: medimos la velocidad con PageSpeed, entendemos los Core Web Vitals y subimos la nota con caché y optimización de imágenes. También repasamos robots.txt, sitemap, canonical y datos estructurados. El objetivo del proyecto: pasar de 75 en PageSpeed.

---

## Recursos

- [Complianz (plugin de cookies)](https://complianz.io/)
- [AEPD - Guía sobre el uso de cookies](https://www.aepd.es/documento/guia-cookies.pdf)
- [Google Consent Mode (documentación)](https://support.google.com/analytics/answer/9976101)
- [Texto del RGPD (BOE / EUR-Lex)](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32016R0679)
- WordPress: `Ajustes > Privacidad` para la política de privacidad
