# S04

## Dominio y DNS | hosting | CMS

### Dominio

- **Dominio** = el nombre que compramos: `marca.com`, `marca.es`.
- Registradores: GoDaddy, Namecheap, Nominalia, IONOS…
- Extensiones: `.com` (global), `.es` (España), `.org`, `.io`…

**SEO y dominios:**

- El dominio no es un factor directo de ranking, pero sí de confianza y de memoria.
- Dominio viejo vs. nuevo: Google premia la antigüedad. No cambies de dominio sin una estrategia.
- Evitar caracteres especiales, guiones dobles, nombres demasiado largos.

### DNS

- **DNS** (Domain Name System) = la guía de teléfonos de Internet. Traduce nombre → IP.
- Tipos de registros:
  - `A`     → apunta a la IP del servidor.
  - `CNAME` → alias (útil para `www`).
  - `MX`    → correo.
  - `TXT`   → verificaciones (Google Search Console, dominio en redes…).

> Cuando configures Google Search Console en S06 vas a tocar un registro TXT. Ya sabéis lo que es.

### Hosting (servidor)

| Tipo                  | Para qué                                  | Ejemplos                      |
| --------------------- | ----------------------------------------- | ----------------------------- |
| Hosting compartido    | Webs pequeñas, bajo coste                 | Hostinger, SiteGround, Raiola |
| VPS                   | Control total, escalable                  | Hetzner, DigitalOcean, Vultr  |
| Cloud                 | Escalabilidad automática                  | AWS, GCP, Azure               |
| Hosting gestionado WP | Solo quieres WordPress sin complicaciones | Kinsta, WP Engine             |

**Velocidad y SEO:** El hosting es el primer factor de velocidad. Un servidor lento → Core Web Vitals malos → peor ranking. La localización del servidor también importa (CDN para audiencias globales).

### CMS

- **CMS** = Content Management System. Te permite crear páginas sin escribir HTML.
- Los más usados: **WordPress** (43% de la web), Wix, Squarespace, Shopify (e-commerce).
- Ventaja: rapidez. Inconveniente: menos control técnico, código más «pesado».
- En S06 veremos cómo optimizar un CMS para SEO técnico.

**Ejercicio rápido:** ¿Quién ya tiene web? ¿Qué CMS usa? ¿Saben cuál es su hosting?

---

### CSS

```html
<link rel="stylesheet" href="estilo.css" />
```

```css
h1 {
  color: blue;
  font-size: 2em;
}
p {
  font-family: Arial, sans-serif;
}
```

- CSS = cómo se _pinta_ el HTML. Separar **estructura** (HTML) de **estilo** (CSS).
- No vamos a profundizar: los CMS lo gestionan casi todo. Lo que sí veremos es cómo el CSS mal cargado penaliza Core Web Vitals (S05).

## Recursos

- [w3schools HTML](https://www.w3schools.com/html/) · [Tryit editor](https://www.w3schools.com/tryit/)
- [w3schools CSS](https://www.w3schools.com/css/)
- [Validador W3C](https://validator.w3.org/)
- [roadmap.sh — Frontend](https://roadmap.sh/frontend)
- [Explicación del DOM (GeeksForGeeks)](https://www.geeksforgeeks.org/html/javascript-html-dom/)
