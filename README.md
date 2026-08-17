## Sitio publicado

https://dsaw-2026-2.github.io/hw-03-css-fundamentals-FrancoUmb-dev/


## Registro de uso de IA

**Prompt utilizado:** le pedí a Claude un `styles.css` externo,
mobile-first (estilos base = móvil, `min-width` para tablet y
escritorio), usando Flexbox/Grid, reutilizando la paleta de colores que
ya habíamos definido a partir de las capturas reales del Figma del
equipo.

**Qué cambió respecto a la primera versión:** la propuesta inicial
usaba una carpeta `styles/` con dos archivos y un acordeón `:target`
para FAQ, siguiendo la descripción general del syllabus. Al comparar
contra el rubric.json real de este repo, encontré que solo se pedía un
único `styles.css` en la raíz, con breakpoints exactos (375px, 768px,
1280px, no rangos genéricos), un archivo nuevo `REFLECTION.md` de
120+ palabras, y que el acordeón de FAQ **no** era un criterio real —
no lo construí, para no perder tiempo en algo que no sumaba puntos.

**Error real que tuve:** al crear `index.html`, VS Code lo guardó como
`index.gtml` por un error de tipeo. GitHub Pages no encontraba ninguna
página que servir hasta que lo renombré correctamente.

**Parte que no entendí de inmediato:** por qué mobile-first con
`min-width` es distinto a `max-width`. Con `min-width`, los estilos sin
media query ya son el diseño móvil, y cada breakpoint solo agrega lo
que cambia hacia arriba, en vez de sobrescribir un diseño de escritorio
pensado primero.

# HW03 — CSS Fundamentals

**Week 3 · DSAW · Universidad de La Sabana**

## Objective

Style your project's landing page with CSS and make it responsive — **no libraries**.

## Deliverables

### `index.html`
The HTML from HW02 (updated if needed).

### `styles.css`
All CSS in an external file. **Zero inline styles** (`style="..."`) anywhere in the HTML.

Must demonstrate:
- Selectors and specificity — not everything styled with element selectors
- Box model: `margin`, `padding`, `border` used intentionally
- **Flexbox or Grid** (or both) for at least one layout section
- **Responsive design** with media queries for:
  - 375px (mobile)
  - 768px (tablet)
  - 1280px (desktop)

### `REFLECTION.md`

Write **at least 120 words** explaining a non-obvious CSS decision you made:
- Why did you choose Grid over Flexbox (or vice versa) for a specific section?
- Why `position: sticky` instead of `fixed`?
- Why did you organize your CSS in the order you did?

Do not describe *what* the CSS does. Explain *why* you made that decision.

## Layer 2

Your `REFLECTION.md` must include a concrete comparison: "If I had used X, the result would have been Y. I chose Z because..."

## AI Log (`AI-LOG.md`)

If you used AI to write CSS:
- Which sections did you generate with AI?
- What did you modify and why?
- What was hardest to understand about the generated CSS?

## Deployment

GitHub Pages — no build step.

## Autograding

The pipeline will check:
- ✅ `index.html`, `styles.css`, `REFLECTION.md` are present
- ✅ HTMLHint + Stylelint pass with no errors
- ✅ GitHub Pages responds with HTTP 200
- ✅ Responsive, Flexbox/Grid, no inline styles, quality reflection (reviewed by Claude)

> **Submission rule:** If it is not deployed and public, it cannot be graded.
