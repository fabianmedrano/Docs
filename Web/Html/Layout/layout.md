
## 🧱 1. Layout fluido a una columna (Mobile‑first)

* **Descripción**: comienza con una sola columna en móvil, que se expande a varias en tablet/desktop vía *media queries*. Ideal para blogs, artículos o landing pages sencillas.
* **Ventajas**: legibilidad, énfasis en contenido principal, fácil de adaptar.
* **Técnica**: CSS Grid o Flexbox con unidades %/em/rem, media queries en anchos clave (mínimo móvil → tablet → escritorio)
* 
 → :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/fluid_to_a_column.html)
---

## 🔲 2. Layout “Holy Grail” – tres columnas

* **Descripción**: cabecera full‑width, tres columnas (sidebar + contenido + sidebar), pie.
* **Uso típico**: dashboard, portal, ecommerce con filtro/especificaciones laterales.
* **Implementación**: grid-template-areas con CSS Grid o Flexbox .
 → :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/Holy_Grail_3_columns.html)
---

## 🃏 3. Tarjetas en cuadrícula (Card/Grid)

* **Descripción**: bloques autónomos dispuestos en fila/columna; flexibles y reorganizables.
* **Ejemplos**: e‑commerce, revistas, tutoriales .
* **Beneficios**: muy responsive, fácil de reordenar y consistentes en distintas pantallas.

(https://fabianmedrano.github.io/Docs/Web/Html/Layout/Grid_cards.html)
---

## 🌓 4. Split-screen (pantallas divididas)

* **Descripción**: pantalla partida en dos bloques verticales (imagen vs texto/CTA) o horizontal.
* **Ideal para**: landing con mensaje fuerte o CTAs destacados.
* **Flexibilidad**: se transforma a una sola columna en móviles, ofrece equilibrio visual.
→ :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/Split‑screen.html)
---

## 🔳 5. Masonry y diseño asimétrico

* **Descripción**: bloques de distinto tamaño, dispuestos de forma irregular/manualmente en Grid.
* **Cuando usarlo**: portfolios o sitios creativos que quieran romper la monotonía ([es.wikipedia.org][4], [seahawkmedia.com][5]).
* **Ventaja**: alto impacto visual y diferenciación de marca.
fluid_to_a_column.html → :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/fluid_to_a_column.html)
---

## 🌐 6. Full-screen o hero inmersivo

* **Descripción**: imagen o vídeo de fondo ocupa todo el viewport, texto minimalista y CTA prominente.
* **Uso ideal**: páginas de producto, startups, portadas.
* **Recomendaciones**: SVGs para logotipos, comprimir imágenes y lazy loading optimizado ([browserstack.com][6]).
fluid_to_a_column.html → :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/fluid_to_a_column.html)
---

## 🪑 7. Modular o cartas móviles

* **Descripción**: diseño compuesto por módulos rectangulares reutilizables (cards/grids).
* **Ventajas**: permite reorganización sencilla de contenidos, adaptación a distintos contenidos.
* **Uso**: home pages de media, portales informativos ([clay.global][7]).
fluid_to_a_column.html → :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/fluid_to_a_column.html)
---

## 🧩 8. Adaptive vs Responsive

* Responsive: un solo layout que cambia con breakpoints.
* Adaptive: versiones separadas por device (ej. mobile/desktop), entregadas por el servidor ([es.wikipedia.org][4], [en.wikipedia.org][8]).
* **Elección**: responsive es más flexible y mantiene mantenimiento simple; adaptive puede mejorar rendimiento en casos complejos.
fluid_to_a_column.html → :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/fluid_to_a_column.html)
---

## ✅ 9. Buenas prácticas comunes

| Elemento      | Recomendación                                                           |
| ------------- | ----------------------------------------------------------------------- |
| Tipografía    | usa rem/em para escalar; base ≈16px                                     |
| Imágenes      | max-width: 100%, srcset o <picture> y formatos eficientes (WebP, SVG)   |
| Botones       | áreas mínimas táctiles 44x44 px; espaciado adecuado                     |
| Lazy‑load     | carga diferida de imágenes y scripts no esenciales                      |
| Grids         | usa CSS Grid/Flexbox con unidades fluidas y breakpoints estratégicos    |
| Mínimo viable | empieza mobile-first: lo esencial en móvil, luego mejoras para desktop  |
fluid_to_a_column.html → :
(https://fabianmedrano.github.io/Docs/Web/Html/Layout/fluid_to_a_column.html)
---

### 🎯 ¿Cómo elegir la base adecuada?

1. **Define el contenido y objetivo** (solo texto, producto, galería, landing, etc.).
2. **Decide la prioridad**: ¿mobile–first o performance intensiva?
3. **Selecciona el layout base**: uno de los anteriores ajustado a tu propósito.
4. **Diseña wireframes**: versión móvil, tablet, escritorio.
5. **Aplica Grid/Flexbox**: fluido, flexible y responsive.
6. **Optimiza rendimiento y UX**: tipografía, imágenes, táctil, lazy‑load, test dispositivos reales ([es.wikipedia.org][4], [indeed.com][9], [logicode.ie][10], [onenine.com][11]).

---

