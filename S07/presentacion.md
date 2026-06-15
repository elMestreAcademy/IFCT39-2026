# SEO on-page + Search Console + tu landing

Sesión S07

---

## Hoy vas a salir con

- Tu SEO on-page entendido y aplicado, no solo "rellenar Yoast".
- Tu sitio dado de alta en Google Search Console, con el sitemap enviado.
- Una landing con barra de navegación, footer propio y estructura por bloques.

---

## Qué es Gutenberg

- Es el editor de bloques de WordPress, el de serie desde 2018.
- Todo es un bloque: párrafo, título, imagen, botón, columnas, vídeo.
- Ya lo usas sin saberlo: donde escribiste tu entrada, eso es Gutenberg.

---

## Vocabulario

| Término            | Qué es                                                   |
| ------------------ | -------------------------------------------------------- |
| Bloque             | Unidad mínima: un párrafo, una imagen, un botón          |
| Patrón             | Composición prefabricada de bloques (un hero, una rejilla) |
| Parte de plantilla | Bloques compartidos por todo el sitio: header, footer    |
| Plantilla          | Esqueleto de un tipo de página: página, entrada, 404     |
| Editor del sitio   | Apariencia > Editor: donde se editan plantillas y partes |

---

## Tema de bloques: Twenty Twenty-Five

- No tiene personalizador clásico ni Apariencia > Menús.
- El header, el footer y los menús se editan con bloques, en el editor del sitio.
- La misma herramienta que usas para el contenido sirve para la estructura. Eso es Full Site Editing.

Trucos de manejo:

- Teclea `/` en una línea vacía para insertar un bloque.
- El icono de vista de lista (arriba a la izquierda) muestra el árbol de bloques.

---

## SEO on-page: la chuleta

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

## Yoast no hace SEO: lo chequea

El semáforo verde solo confirma que has hecho tú el trabajo de la tabla anterior.

---

## Tu turno: aplica la chuleta

Revisa tu landing y tu entrada contra la tabla, fila por fila:

1. Corrige lo que falle. Los alt vacíos y la jerarquía de títulos son lo más común.
2. Añade un enlace interno en cada dirección: la entrada enlaza a la landing y la landing a la entrada. Texto de ancla descriptivo, nada de "pincha aquí".

---

## Search Console: qué es

- Google te cuenta cómo te ve: con qué búsquedas apareces, impresiones, clics, qué páginas indexa y qué errores encuentra.
- Es gratuita y es la fuente de verdad del SEO. Todo lo demás son estimaciones.

---

## Crear la propiedad

En search.google.com/search-console con tu cuenta de Google:

- Tipo "Prefijo de URL" con tu dirección exacta: `https://tu-sitio` (con https y sin barra final).
- No uses el tipo "Dominio": pide verificación por DNS.
- Si tienes hosting propio y controlas el DNS, sí puedes usar "Dominio" y verificar con un registro TXT.

---

## Verificar con Yoast, sin tocar código

1. En Search Console, elige verificación por etiqueta HTML y copia el valor de `content="..."`.
2. En WordPress: Yoast SEO > Ajustes > Conexiones del sitio > pega en el campo de Google > Guardar.
3. Vuelve a Search Console y pulsa Verificar.

---

## Sitemap e indexación

1. Abre `https://tu-sitio/sitemap_index.xml`: ese índice lo genera Yoast.
2. En Search Console: Sitemaps > Añadir sitemap > `sitemap_index.xml` > Enviar.
3. Inspección de URL: pega la URL de tu landing > Solicitar indexación. Repite con la entrada.

La indexación tarda días y los primeros datos de búsquedas, semanas. Hoy plantamos.

---

## Tu landing: página de inicio estática

Ajustes > Lectura > Una página estática > elige tu landing como "Página de inicio".

Así tu landing responde en la raíz del dominio.

---

## Barra de navegación (header)

1. Apariencia > Editor > Patrones > Partes de plantilla > Cabecera.
2. Localiza el bloque Navegación. Si no está, insértalo junto al título del sitio.
3. Añade enlaces: Inicio, Servicios, Sobre mí, Contacto. Las que no existan, créalas como borrador desde el propio bloque.
4. Guarda. El header es parte de plantilla: el cambio afecta a todo el sitio.

Extra: pon el header fijo (sticky) para que acompañe al hacer scroll.

---

## Footer

1. Apariencia > Editor > Patrones > Partes de plantilla > Pie de página.
2. Quita o reescribe los créditos por defecto.
3. Deja un footer mínimo digno: nombre y tagline, bloque de iconos sociales con tus redes, y un segundo bloque de navegación con enlaces secundarios.

---

## Cuerpo de la landing con patrones

Edita tu landing y componla con patrones (insertador > pestaña Patrones):

- Hero arriba: bloque Cubierta con imagen de fondo + H1 + botón CTA.
- Una sección de columnas: 3 servicios, 3 razones o 3 productos.
- Un CTA final con botón.

Recuerda la chuleta: el H1 del hero lleva la keyword y los títulos de sección son H2.

---

## Para ir más allá: CSS sobre tu sitio (opcional)

De menos a más:

1. Estilos globales sin CSS: Apariencia > Editor > Estilos. Cambia paleta, tipografías y prueba las variaciones de estilo de un clic.
2. CSS adicional global: Estilos > menú de tres puntos > CSS adicional. Caja de CSS con vista previa en vivo.
3. Clase propia: selecciona un bloque > Avanzado > Clases CSS adicionales > escribe `boton-cta`, y dale estilo:

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

Orden para no pelearte con el tema: primero la interfaz, luego el CSS.

---

## Al terminar hoy tienes

- On-page aplicado en tu landing y tu entrada.
- Sitio verificado en Search Console, sitemap enviado e indexación solicitada.
- Landing con navegación, footer propio y estructura por patrones.

---

## Para la próxima

- Termina la landing si te quedaste: header + footer + hero como mínimo.
- Publica una página nueva (Servicios o Sobre mí) pasándole la chuleta on-page antes.
- Entra a Search Console y mira Indexación > Páginas: ¿aparece ya algo?

---

## Enlaces

- Google Search Console: search.google.com/search-console
- El editor del sitio: wordpress.org/documentation/article/site-editor
- Biblioteca de patrones: wordpress.org/patterns
