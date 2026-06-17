---
marp: true
paginate: true
---

# Normativa: cookies, RGPD y consentimiento

Sesión Normativa

---

## Hoy

En algunos asos: el sitio todavía no es legal: GA4 carga sin pedir permiso. Al finalizar conseguiremos:

- Un banner de cookies con aceptar y rechazar al mismo nivel.
- Las tres páginas legales publicadas: privacidad, cookies y aviso legal.
- GA4 bajo consentimiento: solo mide cuando el visitante acepta.
- Un footer legal con los enlaces y la opción de revocar.

---

## Requisitos de sesiones anteriores

- GA4 instalado y recogiendo datos vía Site Kit (S09).
- La cuenta de Google lista, la misma de Search Console y GA4.
- El contenido de la página de Contacto pensado o redactado.

Si falta algo, eso es lo primero de hoy.

---

## Por qué es obligatorio

No es una buena práctica opcional: es ley. Tres normas nos afectan:

- **RGPD**: el reglamento europeo de protección de datos.
- **LOPDGDD**: la ley española que lo desarrolla.
- **LSSI-CE**: obliga al aviso legal y regula las cookies.

El consentimiento debe ser previo, informado, granular y revocable.


---

## La regla de las cookies

- Las cookies **técnicas** (las que hacen funcionar el sitio) no necesitan permiso.
- Las de **analítica, publicidad o seguimiento** sí: GA4 entra aquí.
- No pueden cargar hasta que el visitante acepta.

**Rechazar tiene que ser tan fácil como aceptar.** Esconder el botón de rechazar es ilegal, y la AEPD multa por ello.

[politica-cookies-adatada-rgpd](https://textos-legales.edgartamarit.com/politica-cookies-adatada-rgpd/)

---

## Los tres documentos

| Documento              | Qué dice                                      |
| ---------------------- | --------------------------------------------- |
| Aviso legal            | Quién es el titular: nombre, NIF, contacto    |
| Política de privacidad | Qué datos se recogen, para qué y los derechos |
| Política de cookies    | Qué cookies hay, de quién y cuánto duran      |

El banner es la puerta; estas tres páginas son la letra pequeña a la que enlaza.

---

## Complianz: instalar el banner

1. `Plugins > Añadir nuevo > "Complianz | GDPR/CCPA Cookie Consent" > Instalar > Activar`.
2. Asistente de Complianz:
   - Región: solo **Europa**.
   - Servicios: marcamos **Google Analytics**.
   - Consentimiento: **Opt-in** (nada carga hasta aceptar).
3. **Escaneo de cookies**: Complianz lista las cookies del sitio.
4. El banner, con tres opciones al mismo nivel: **Aceptar**, **Rechazar**, **Preferencias**.

---

## Comprobar el banner

Abrimos el sitio en una pestaña de **incógnito**.

El banner debe saltar antes de poder navegar. Si no aparece, revisamos que Complianz esté activado y el banner publicado.

---

## Las páginas legales

- **Política de cookies**: ya la generó Complianz.
- **Política de privacidad**: WordPress trae un borrador en `Ajustes > Privacidad`. La revisamos y mencionamos a Google como encargado y los derechos del usuario.
- **Aviso legal**: lo redactamos con los datos del titular. Sin huecos sin completar.

Las tres quedan publicadas.

---

## Modo de consentimiento sobre GA4

El meollo: que GA4 no cargue hasta que el visitante acepta.

- **Google Consent Mode**: GA4 espera la señal de consentimiento.
- Lo activamos en `Complianz > Integraciones`.
- Antes de aceptar: GA4 no usa cookies ni identifica.
- Tras aceptar: GA4 mide con normalidad.

---

## Comprobar el consentimiento

1. Incógnito: salta el banner y GA4 en Tiempo real no cuenta la visita.
2. Pulsamos **Aceptar**, recargamos: ahora sí aparece en Tiempo real.
3. En otra ventana, pulsamos **Rechazar**: comprobamos que respeta el "no".

Este es el motivo por el que ayer instalamos GA4 sin banner y hoy lo dejamos conforme.

---

## Footer legal

Dejamos los enlaces siempre a la vista:

- En `Apariencia > Widgets` o el editor del tema, añadimos al footer: **Aviso legal**, **Política de privacidad** y **Política de cookies**.
- Comprobamos el enlace de **Gestionar consentimiento**: el visitante puede cambiar de opinión, porque el consentimiento es revocable.

---

## Al finalizar conseguiremos

- Banner de cookies funcionando, con aceptar y rechazar al mismo nivel.
- Las tres páginas legales publicadas.
- GA4 bajo modo de consentimiento: solo mide tras la aceptación.
- Footer legal con los enlaces y la opción de revocar.

---

## Para la próxima

- Probamos el banner desde casa en incógnito: aparece y rechazar funciona.
- Rellenamos los datos del aviso legal, sin huecos.
- No instalamos plugins de más: cada plugin pesa, y la próxima sesión va de **velocidad**.

La próxima: **SEO técnico y velocidad**. Medimos PageSpeed y subimos la nota por encima de 75.

---

## Enlaces

- Complianz: complianz.io
- AEPD, guía de cookies: aepd.es
- Google Consent Mode: support.google.com/analytics
