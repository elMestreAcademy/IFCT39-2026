# Finalizar el sitio y darlo de alta en Search Console

Sesión S08

---

## Hoy

Terminamos el sitio y lo damos de alta en Google Search Console. Al finalizar conseguiremos:

- La Landing terminada: header, footer y hero.
- Una página nueva publicada (Servicios o Sobre mí) con su on-page.
- On-page fino en al menos 2 URLs, enlazadas entre sí.
- El sitio dado de alta en Search Console, con el sitemap enviado.
- Un retoque de estilo con CSS sobre el sitio.

---

## Requisitos de sesiones anteriores

- La Landing publicada y puesta como página de inicio estática.
- On-page aplicado en la Landing y en la entrada (Yoast configurado).
- La cuenta de Google lista para usar.

Si falta algo, eso es lo primero de hoy.

---

## Recordatorio: la chuleta on-page

| Elemento         | Regla                                                  |
| ---------------- | ------------------------------------------------------ |
| SEO title        | 50-60 caracteres, keyword al principio, marca al final |
| Meta description | 120-155 caracteres, keyword + invitación al clic       |
| Slug             | Corto, con keyword, sin preposiciones ni fechas        |
| H1               | Uno solo por página, es el título                      |
| H2 / H3          | Jerarquía real, con variaciones de la keyword          |
| Primer párrafo   | La keyword en las primeras 100 palabras                |
| Imágenes         | Atributo alt descriptivo                               |
| Enlazado interno | Cada página enlaza al menos a otra del sitio           |

---

## Estación 1: finalizar la Landing

- **Header**: navegación con Inicio, Servicios, Sobre mí, Contacto. Guardar (afecta a todo el sitio).
- **Footer**: nombre y tagline, iconos sociales con las redes, créditos por defecto fuera.
- **Hero**: bloque Cubierta con imagen de fondo, H1 con la keyword y botón CTA.

---

## Estación 2: una página nueva

Creamos **Servicios** o **Sobre mí**. Antes de publicar, le pasamos la chuleta:

- title y meta description en Yoast.
- slug corto con keyword.
- un solo H1; H2 para las secciones.
- alt descriptivo en las imágenes.

---

## Estación 3: enlazado interno

- Esta nueva página enlaza a Landing.
- Landing o la entrada enlaza a la nueva página.
- Texto de ancla descriptivo, nada de "pincha aquí".

Con esto conseguimos **on-page fino en 2 URLs o más**, el objetivo del día.

---

## Google Search Console: qué es

- Google nos cuenta cómo nos ve: con qué búsquedas aparecemos, impresiones, clics, qué páginas indexa y qué errores encuentra.
- Es gratuita y es la fuente de verdad del SEO. Todo lo demás son estimaciones.
- Hoy la damos de alta por primera vez.

---

## Crear la propiedad

En search.google.com/search-console con la cuenta de Google:

- Tipo "Prefijo de URL" con la dirección exacta: `https://tu-sitio` (con https y sin barra final).
- No usar el tipo "Dominio": pide verificación por DNS.
- Con hosting propio y control del DNS, sí se puede usar "Dominio" y verificar con un registro TXT.

---

## Verificar con Yoast, sin tocar código

1. En Search Console, elegir verificación por etiqueta HTML y copiar el valor de `content="..."`.
2. En WordPress: Yoast SEO > Ajustes > Conexiones del sitio > pegar en el campo de Google > Guardar.
3. Volver a Search Console y pulsar Verificar.

---

## Enviar el sitemap

1. Abrir `https://tu-sitio/sitemap_index.xml`: ese índice lo genera Yoast.
2. En Search Console: Sitemaps > Añadir sitemap > `sitemap_index.xml` > Enviar.

---

## Solicitar indexación

- Inspección de URL: pegar la URL de la Landing > Solicitar indexación. Repetir con la página nueva.
- La indexación tarda días y los primeros datos de búsquedas, semanas. Hoy plantamos.

---

## Estilo con CSS

De menos a más:

1. **Estilos globales sin CSS**: Apariencia > Editor > Estilos. Paleta, tipografías y variaciones de estilo de un clic.
2. **CSS adicional global**: Estilos > menú de tres puntos > CSS adicional. Vista previa en vivo.
3. **Clase propia**: seleccionamos un bloque > Avanzado > Clases CSS adicionales > escribimos `boton-cta`, y le damos estilo:

---

## Estilo con CSS

Orden para no pelearse con el tema: primero la interfaz, luego el CSS.

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

---

## Al finalizar conseguiremos

- Landing terminada y una página nueva publicada.
- On-page fino en 2 URLs o más, enlazadas entre sí.
- Sitio verificado en Search Console, sitemap enviado e indexación solicitada.
- El sitio con un toque de estilo propio.

---

## Para la próxima

- Entrar a Search Console desde casa y mirar Indexación > Páginas: ¿aparece ya algo?
- La próxima sesión instalamos la **analítica (GA4)** para medir visitas y montamos el **banner de cookies** para estar en regla.

---

## Enlaces

- Google Search Console: search.google.com/search-console
- El editor del sitio: wordpress.org/documentation/article/site-editor
- Biblioteca de patrones: wordpress.org/patterns
