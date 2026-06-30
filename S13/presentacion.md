---
marp: true
paginate: true
---

# GEO: posicionarse en los buscadores con IA

S13

---

## Estado esperado

En S11 vimos el GEO por encima: qué es y tres acciones rápidas sobre una página.

Hoy lo trabajamos a fondo. Al finalizar conseguiremos:

- Entender **cómo decide una IA a quién cita**.
- Dejar el sitio **legible para los crawlers de IA**.
- Publicar un **`llms.txt`** y un primer **schema**.
- Saber **medir** si nos mencionan ChatGPT, Perplexity o Gemini.

---

## Requisitos de sesiones anteriores

- El sitio publicado, rápido y rastreable (S10).
- El **mapa de keywords y clusters** de S11.
- Las páginas principales con on-page hecho y alguna **FAQ**.
- GA4 instalado y recogiendo datos (S09).

---

## Recordatorio: qué es el GEO

GEO es **Generative Engine Optimization**: optimizar para los buscadores que **responden con IA** en lugar de devolver solo una lista de enlaces.

El SEO pelea por un puesto en la lista azul.
El GEO pelea por **ser la fuente que la IA usa para redactar la respuesta**.

No son rivales: el GEO se construye **encima** de un buen SEO.

---

## SEO frente a GEO

|                | SEO                          | GEO                                   |
| -------------- | ---------------------------- | ------------------------------------- |
| Resultado      | Lista de enlaces             | Respuesta redactada con citas         |
| Objetivo       | Subir de puesto              | Ser citado como fuente                |
| Métrica        | Posición, clics              | Menciones y citas                     |
| Unidad de éxito| La **página**                | El **párrafo extraíble**              |
| Premia         | Autoridad + relevancia       | Claridad + estructura + datos         |

---

## Por qué importa ahora

- Google muestra **AI Overviews** sobre muchísimas búsquedas.
- **ChatGPT, Perplexity y Gemini** ya se usan como buscador.
- En esas respuestas, la mayoría de la gente **no baja a la web**: lee el resumen.

Si no estás en el resumen, para ese usuario **no existes**, aunque seas el primero en Google.

---

## Cómo funciona un buscador con IA

Tres fases. Hay que ganar en las tres:

1. **Rastreo**: un bot de IA lee tu web (o usa el índice de Google).
2. **Recuperación**: ante una pregunta, el sistema busca y recoge **trozos** de páginas relevantes.
3. **Síntesis y cita**: el modelo redacta una respuesta con esos trozos y enlaza algunas fuentes.

GEO = facilitar las tres: que te lean, que te recuperen, que te citen.

---

## Dos maneras de aparecer

- **En el entrenamiento del modelo**: tu contenido formó parte de lo que aprendió. Lento, indirecto, sin control.
- **En la búsqueda en vivo (grounding)**: el sistema busca en tiempo real y cita lo que encuentra hoy.

Trabajamos sobre todo la **segunda**: es la que premia un contenido bien estructurado y la que da resultados a corto plazo.

---

## El cambio de mentalidad

Antes escribíamos para **convencer a una persona** que llega a la página.

Ahora, además, escribimos para que una IA pueda **entender, extraer y reutilizar** un fragmento sin malinterpretarlo.

La pregunta nueva en cada bloque de texto:

> ¿Podría una IA copiar esta frase como respuesta y quedar bien?

---

## Citabilidad: qué hace que te citen

Un pasaje es **citable** cuando se sostiene solo, fuera de su página.

Características de un párrafo citable:

- Responde **una** pregunta concreta.
- Es **autocontenido**: se entiende sin el resto de la página.
- Empieza por la **respuesta**, no por el rodeo.
- Incluye un **dato**: cifra, plazo, precio orientativo, paso.
- Usa **lenguaje claro**, sin jerga interna.

---

## Anatomía de un bloque citable

El patrón que mejor funciona:

```text
## ¿Cuánto cuesta una limpieza facial en Valencia?

Una limpieza facial profesional en Valencia cuesta entre 40 y 70 euros
según el tipo de piel y los extras. La sesión dura unos 60 minutos.

[luego ya el detalle, el proceso, los matices...]
```

Encabezado = la pregunta. Primera frase = la respuesta. Después, el desarrollo.

---

## Antes y después

**Antes (no citable):**

> En nuestro centro apostamos por cuidar tu piel con los mejores tratamientos y un trato cercano y personalizado.

**Después (citable):**

> Una limpieza facial profunda elimina puntos negros e impurezas en una sesión de 60 minutos. Recomendada cada 4 a 6 semanas para pieles mixtas.

El segundo tiene **sujeto, dato y plazo**. La IA lo puede usar tal cual.

---

## La regla de la respuesta primero

Estructura cada sección como **pregunta -> respuesta corta -> desarrollo**.

- El encabezado plantea una duda real (sale de tu mapa de keywords).
- La primera o dos primeras frases la responden de forma directa.
- El resto amplía para quien quiera profundizar.

Es bueno para la IA y también para la persona con prisa.

---

## Crawlers de IA: quién te lee

Cada plataforma manda su propio bot. Conviene conocerlos:

| Bot                | De quién       | Para qué                          |
| ------------------ | -------------- | --------------------------------- |
| `Googlebot`        | Google         | Índice de Google y AI Overviews   |
| `Google-Extended`  | Google         | Entrenar Gemini (no afecta a AIO) |
| `GPTBot`           | OpenAI         | Entrenar modelos                  |
| `OAI-SearchBot`    | OpenAI         | Búsqueda dentro de ChatGPT        |
| `ClaudeBot`        | Anthropic      | Entrenar y responder de Claude    |
| `PerplexityBot`    | Perplexity     | Indexar para Perplexity           |
| `Bingbot`          | Microsoft      | Bing y Copilot                    |

---

## robots.txt: el dilema

`robots.txt` decide **qué bots pueden entrar**. Para GEO hay una tensión:

- **Permitir** los bots de IA = posibilidad de ser citado.
- **Bloquearlos** = proteges tu contenido, pero desapareces de esas respuestas.

Para un negocio que quiere visibilidad, la regla general es **permitir** los bots de búsqueda con IA.

Aviso clave: si bloqueas **Googlebot**, te caes de Google **y** de AI Overviews a la vez.

---

## robots.txt de ejemplo

Permitir todo lo de búsqueda y dejar fuera solo lo que no quieras para entrenamiento:

```text
# Buscadores y búsqueda con IA: bienvenidos
User-agent: Googlebot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: PerplexityBot
Allow: /

# Si NO quieres ceder contenido para entrenar modelos:
User-agent: GPTBot
Disallow: /

Sitemap: https://tudominio.com/sitemap.xml
```

---

## llms.txt: la guía para modelos

`llms.txt` es un archivo en la **raíz** del sitio (`tudominio.com/llms.txt`) que resume, en Markdown, **qué eres y cuáles son tus páginas clave**.

Para qué sirve:

- Dar a la IA un **mapa limpio** del sitio.
- Destacar el contenido que importa.
- Reducir el ruido de menús, banners y plantilla.

No es obligatorio ni garantiza nada, pero es barato de hacer y cada vez más sistemas lo miran.

---

## Anatomía de un llms.txt

```text
# Nombre del sitio o negocio

> Una frase que diga qué ofreces y a quién.

## Servicios
- [Servicio principal](url): qué resuelve, en una línea
- [Otro servicio](url): idem

## Recursos
- [FAQ](url): preguntas frecuentes
- [Sobre nosotros](url): experiencia y autoridad
```

H1 = nombre. Blockquote = resumen. H2 = secciones con enlaces y descripción.

---

## llms.txt de ejemplo

```text
# Estudio Foto Granada

> Fotografía de bodas y embarazo en Granada. Reportajes naturales,
> entrega en 3 semanas, cobertura en toda la provincia.

## Servicios
- [Bodas](https://ejemplo.com/bodas): reportaje completo, precios y proceso
- [Embarazo](https://ejemplo.com/embarazo): sesiones en estudio y exterior

## Recursos
- [FAQ](https://ejemplo.com/faq): dudas habituales y precios orientativos
- [Sobre mí](https://ejemplo.com/sobre-mi): 10 años de experiencia y estilo
```

---

## Datos estructurados para IA

Los **datos estructurados** (Schema.org, en formato JSON-LD) le dicen a la máquina **qué es cada cosa** sin tener que adivinarlo.

Ayudan a la IA a:

- Identificar tu **entidad** (negocio, persona, marca).
- Entender tus **FAQs** como preguntas y respuestas.
- Conectar tu sitio con tus **perfiles externos**.

En WordPress, gran parte la pone **Yoast** sola; las FAQs salen del bloque de FAQ (lo vimos en S10).

---

## Qué schemas importan para GEO

| Schema           | Para qué sirve                                   |
| ---------------- | ------------------------------------------------ |
| `Organization`   | Identificar el negocio como entidad              |
| `Person`         | Identificar al profesional o autor               |
| `FAQPage`        | Marcar preguntas y respuestas                    |
| `Article`        | Marcar entradas y guías                          |
| `sameAs`         | Enlazar con tus perfiles oficiales               |
| `speakable`      | Señalar lo apto para asistentes de voz           |

---

## Ejemplo: Organization + sameAs

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Estudio Foto Granada",
  "url": "https://ejemplo.com",
  "telephone": "+34 600 000 000",
  "address": "Calle Mayor 1, Granada",
  "sameAs": [
    "https://instagram.com/estudiofotogranada",
    "https://g.page/estudiofotogranada"
  ]
}
```

`sameAs` le dice a la IA: "estos perfiles también soy yo".

---

## Ejemplo: FAQPage

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "¿Cuánto cuesta un reportaje de boda?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "Desde 1.200 euros, según horas de cobertura y entrega."
    }
  }]
}
```

La misma FAQ sirve para Google y para la IA.

---

## Entidades: que sepan quién eres

La IA no razona con páginas sueltas, sino con **entidades**: negocios, personas, lugares.

Para que te reconozca como una entidad clara:

- Usa **siempre el mismo nombre** (web, redes, Google).
- Mantén **NAP** consistente: Nombre, dirección y teléfono iguales en todas partes.
- Enlaza tus perfiles con `sameAs`.
- Ten una **ficha de Google** (Google Business Profile) viva.

Un negocio coherente en toda la red es un negocio **fácil de citar**.

---

## Menciones y autoridad (E-E-A-T para IA)

La IA confía más en quien aparece **mencionado en sitios creíbles**, no solo en tu propia web.

Lo que suma:

- Menciones en **prensa local, directorios serios y asociaciones**.
- **Reseñas** reales y consistentes.
- Un autor identificable con experiencia demostrable.
- Coherencia entre lo que dices ser y lo que dicen de ti fuera.

No se trata de enlaces a cualquier precio, sino de **presencia creíble y repetida**.

---

## Optimizar por plataforma

El fondo es común (claridad, estructura, datos), pero cada motor tiene su sesgo:

- **Google AI Overviews**
- **ChatGPT (búsqueda)**
- **Perplexity**
- **Gemini**
- **Bing Copilot**

Vamos una por una, en lo práctico.

---

## Google AI Overviews y Gemini

**AI Overviews:**

- Bebe del **índice normal de Google**: buen SEO = base imprescindible.
- Premia respuestas directas, FAQs y datos estructurados.
- Bloquear Googlebot te saca también de aquí.

**Gemini:**

- Hereda la lógica del ecosistema Google.
- Ayuda la autoridad y la presencia rastreable.

---

## ChatGPT, Perplexity y Copilot

- **ChatGPT (búsqueda)**: usa su propio bot (`OAI-SearchBot`) y cita fuentes. Premia contenido claro, reciente y consistente.
- **Perplexity**: es el que **más cita**. Le encantan las páginas específicas y bien delimitadas; aquí la citabilidad rinde mucho.
- **Bing Copilot**: depende del índice de **Bing**. Conviene estar dado de alta en **Bing Webmaster Tools**, no solo en Google.

---

## Resumen por plataforma

| Plataforma     | Se apoya en        | Qué priorizar                    |
| -------------- | ------------------ | -------------------------------- |
| AI Overviews   | Índice de Google   | SEO sólido + FAQs + schema       |
| Gemini         | Ecosistema Google  | Autoridad + estructura           |
| ChatGPT        | OAI-SearchBot      | Claridad + frescura              |
| Perplexity     | PerplexityBot      | Páginas específicas y citables   |
| Copilot        | Índice de Bing     | Alta en Bing + datos claros      |

---

## Medir: ¿me están citando?

El GEO también se mide, aunque todavía no haya un panel perfecto. Tres vías:

1. **Tráfico de IA en GA4**: visitas que llegan desde dominios de IA.
2. **Test manual**: preguntar a los modelos por tu nicho y ver quién sale.
3. **Reseñas de marca**: buscarte por nombre en cada asistente.

---

## Tráfico de IA en GA4

En GA4, el tráfico de asistentes llega como **referral** desde dominios como:

- `chatgpt.com`
- `perplexity.ai`
- `gemini.google.com`
- `copilot.microsoft.com`

En **Adquisición**, filtra por esos orígenes para ver cuántas visitas te manda la IA. Aún es poco, pero crece.

---

## Test manual de visibilidad

La forma más directa de saber si apareces: **preguntar**.

En ChatGPT, Perplexity y Gemini, haz 3 preguntas como las haría tu cliente:

- "¿Mejor [tu servicio] en [tu ciudad]?"
- "¿Cuánto cuesta [tu servicio]?"
- "Recomiéndame un [tu profesión] en [tu zona]."

Apunta: ¿sales? ¿te citan? ¿a quién citan en tu lugar?

---

## Errores comunes en GEO

- Texto de relleno y promesas vagas, sin un solo dato.
- Encabezados decorativos ("Bienvenidos") en vez de preguntas reales.
- Una home gigante que intenta cubrirlo todo.
- Bloquear sin querer a los bots en `robots.txt`.
- Nombre y datos distintos en cada sitio (entidad confusa).
- Copiar contenido genérico de IA: lo que abunda, no se cita.

---

## Checklist GEO

- [ ] Encabezados que son **preguntas** reales.
- [ ] Respuesta **directa** bajo cada encabezado.
- [ ] **Datos** concretos: cifras, plazos, precios orientativos.
- [ ] **FAQs** con datos estructurados.
- [ ] **Schema** de Organization o Person con `sameAs`.
- [ ] **`llms.txt`** publicado en la raíz.
- [ ] `robots.txt` que **deja entrar** a la búsqueda con IA.
- [ ] Nombre y NAP **consistentes** dentro y fuera.

---

## Taller: hoy sobre tu proyecto

Cinco acciones, cada una sobre tu sitio real:

1. Publicar un **`llms.txt`**.
2. Añadir un **schema** (Organization o Person).
3. Reescribir **una página** para que sea citable.
4. Revisar **`robots.txt`** y el acceso de los bots.
5. Hacer el **test de visibilidad** en los tres asistentes.

---

## Acción 1: llms.txt

- Coge el mapa de keywords de S11.
- Redacta el `llms.txt`: nombre, frase resumen, y las 4 a 6 URLs clave con su descripción.
- Súbelo a la raíz: `tudominio.com/llms.txt`.

Plantilla mínima:

```text
# [Tu negocio]
> [Qué ofreces, a quién, dónde]
## Servicios
- [Página](url): una línea
```

---

## Acción 2: schema

- Si usas **Yoast**, revisa que ya emite `Organization` o `Person`: completa nombre, logo y perfiles (`sameAs`).
- Marca al menos **una FAQ** con el bloque de FAQ para que salga como `FAQPage`.
- Comprueba el resultado en el **Rich Results Test** de Google.

---

## Acción 3: reescribir para citabilidad

Elige una página de servicio y, en su sección principal:

1. Cambia el encabezado por una **pregunta** real.
2. Pon debajo una **respuesta de una o dos frases** con un dato.
3. Deja el desarrollo después.

Esa primera frase es la que una IA puede copiar como respuesta.

---

## Acción 4 y 5: acceso y visibilidad

**Acceso:**

- Abre `tudominio.com/robots.txt`.
- Confirma que **no** bloqueas Googlebot ni los bots de búsqueda con IA.

**Visibilidad:**

- Haz las 3 preguntas tipo en ChatGPT, Perplexity y Gemini.
- Anota si sales y a quién citan. Es tu **línea base** de hoy.

---

## Al finalizar conseguiremos

- `llms.txt` publicado en el sitio.
- Un schema activo con `sameAs`.
- Una página reescrita para ser citable.
- `robots.txt` revisado.
- Una primera **medición** de visibilidad en IA.

Eso es el hito GEO del proyecto.

---

## Para la próxima

- Reescribir **dos páginas más** con el patrón pregunta-respuesta.
- Completar el `llms.txt` con todas las URLs importantes.
- Dar de alta el sitio en **Bing Webmaster Tools**.
- Repetir el **test de visibilidad** en una semana y comparar.

---

## Enlaces

- [Esquema llms.txt](https://llmstxt.org)
- [Schema.org](https://schema.org)
- [Rich Results Test](https://search.google.com/test/rich-results)
- [Bing Webmaster Tools](https://www.bing.com/webmasters)
- [Perplexity](https://www.perplexity.ai)
- [Gemini](https://gemini.google.com)
- [ChatGPT](https://chatgpt.com)
