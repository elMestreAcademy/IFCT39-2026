# S06 -- WordPress: primer contacto (guion de rescate)

> Todos tienen al menos una pagina publicada.
> Gutenberg ha costado; customizacion ha robado tiempo.
> Objetivo del tramo restante: hacer SEO visible sobre lo que ya tienen.

---

## Cronograma restante

| Min | Bloque                                              |
| --- | --------------------------------------------------- |
| 10  | Checkpoint: 3 cosas que si o si tienen que estar    |
| 30  | Yoast en vivo sobre su propia pagina publicada      |
| 10  | Descanso                                            |
| 20  | Paginas vs entradas (teoria minima)                 |
| 30  | Trabajo individual: crear una entrada               |
| 10  | Cierre, deberes y conexion con S07                  |

---

## Checkpoint (10 min)

En paralelo, cada uno verifica. Si alguien tiene problema, lo resolvemos en voz alta:

1. **Yoast instalado y activo** -- aparece en el menu lateral izquierdo como "SEO".
   Si no: `Plugins > Añadir nuevo > "Yoast SEO" > Instalar > Activar`.

2. **Permalinks en `/%postname%/`** -- `Ajustes > URLs > Estructura personalizada`.
   Si no: cambiarlo ahora. Afecta a todas las URLs del sitio.

3. **Pagina publicada visible** -- abrir la URL publica en una pestana del navegador y confirmar que carga.

---

## Yoast en vivo sobre su propia pagina (30 min)

### Demo en pantalla (10 min)

Abrir la pagina publicada en modo edicion. Bajar hasta el panel de Yoast al final del editor.

Dos pestanas:

- **SEO**: semaforo, keyword principal, preview del snippet tal como lo veria Google.
- **Legibilidad**: estructura de titulos, longitud de parrafos.

Explicar el snippet -- es lo que Google muestra en los resultados de busqueda:

- **SEO title**: el `<title>` de la pagina. Por defecto usa el titulo del post + nombre del sitio.
- **Slug**: la parte de la URL despues del dominio. Corto, con la keyword, sin preposiciones.
- **Meta description**: el texto gris bajo el titulo. No rankea directamente, pero sube el CTR.

### Ejercicio guiado (20 min)

Cada uno edita su pagina ya publicada y hace estos 3 cambios en el panel de Yoast:

1. Escribe su **keyword principal** en el campo "Frase clave".
2. Ajusta el **SEO title** para que incluya la keyword de forma natural.
3. Escribe una **meta description** de 120-155 caracteres con la keyword y que invite a hacer clic.

Rotar por las mesas. Meta: al menos un circulo verde en el semaforo de Yoast antes de continuar.

---

## Paginas vs entradas (20 min)

Teoria minima, solo lo que necesitan para el ejercicio siguiente:

| Concepto   | Paginas                              | Entradas                                 |
| ---------- | ------------------------------------ | ---------------------------------------- |
| Para que   | Contenido estatico del sitio         | Articulos del blog, contenido fresco     |
| URL tipica | `/sobre-mi/`, `/servicios/`          | `/recetas/tortilla-sin-cebolla/`         |
| SEO        | Jerarquia del sitio, keywords clave  | Cola larga, volumen, actualizaciones     |
| Ejemplos   | Inicio, Contacto, Sobre mi           | Articulos, guias, tutoriales, noticias   |

**Para SEO necesitamos las dos**: paginas como esqueleto + entradas como musculo.

Lo que ya tienen (la landing) es una pagina. Ahora van a crear su primera entrada.

---

## Trabajo individual: primera entrada (30 min)

Crear una entrada de blog en `Entradas > Añadir nueva`.

Requisitos minimos:

- Titulo que contenga una keyword real de su proyecto.
- Al menos 2 parrafos de texto y un H2.
- Rellenar el campo "Frase clave" de Yoast con esa keyword.
- Publicar (no dejar en borrador).

No importa que sea perfecto. En S08 haremos SEO on-page encima de esto.

Rotar y ayudar con Gutenberg donde se atasquen -- el objetivo es publicar, no maquetar.

---

## Cierre (10 min)

### Que tienen hoy

- WordPress operativo con Yoast configurado.
- Permalinks bien puestos.
- Una pagina + una entrada publicadas con snippet editado.

### Deberes para S07

1. Escribir 3 ideas de titulos de entradas para su proyecto (pensados como busquedas reales, no como titulos de redes sociales). Ejemplo: no "Mi viaje a Roma" sino "que ver en Roma en 3 dias con ninos".
2. Tener acceso a la cuenta de Google que usaran para Search Console (la misma del proyecto, no una personal si pueden).

### S07

**Google Search Console**: verificar la propiedad del sitio, enviar el sitemap, ver las primeras queries. Es la herramienta que nos dira que busca la gente para llegar a nuestra web.

---

## Plugins pendientes (no instalar hoy)

Quedan para sesiones proximas para no saturar:

- **Site Kit by Google** (GA4 + Search Console) -- S07/S09
- **WP Super Cache / LiteSpeed Cache** (velocidad) -- SEO tecnico
- **Complianz / CookieYes** (GDPR) -- cuando conectemos GA4
