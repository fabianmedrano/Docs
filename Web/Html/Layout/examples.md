

## 1. **Layout fluido a una columna (Mobile‑first)**

```html
<!-- index.html -->
<div class="container">
  <article>Contenido principal...</article>
  <aside>Contenido secundario</aside>
</div>
<style>
.container {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;
}
@media (min-width: 600px) {
  .container {
    grid-template-columns: 2fr 1fr;
  }
}
</style>
```

---

## 2. **Holy Grail (tres columnas)**

```html
<div class="container">
  <header>Header</header>
  <nav>Nav</nav>
  <main>Main</main>
  <aside>Aside</aside>
  <footer>Footer</footer>
</div>
<style>
.container {
  display: grid;
  grid-template-areas:
    "header header header"
    "nav content aside"
    "footer footer footer";
  grid-template-columns: 200px 1fr 200px;
  grid-template-rows: auto 1fr auto;
  height: 100vh;
  gap: 10px;
}
header { grid-area: header; }
nav    { grid-area: nav; }
main   { grid-area: content; }
aside  { grid-area: aside; }
footer { grid-area: footer; }
@media (max-width: 768px) {
  .container {
    grid-template-areas:
      "header"
      "nav"
      "content"
      "aside"
      "footer";
    grid-template-columns: 1fr;
  }
}
</style>
```

Este ejemplo está adaptado del tutorial de DigitalOcean ([digitalocean.com][1], [medium.com][2]).

---

## 3. **Tarjetas en cuadrícula (Card/Grid)**

```html
<ul class="card-grid">
  <li class="card">Tarjeta 1</li>
  <li class="card">Tarjeta 2</li>
  <li class="card">Tarjeta 3</li>
</ul>
<style>
.card-grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
}
.card {
  border: 1px solid #ccc;
  padding: 1rem;
}
</style>
```

Ejemplo basado en MDN para auto-placement ([developer.mozilla.org][3]).

---

## 4. **Split‑screen (pantalla dividida)**

```html
<div class="split">
  <div class="left">Texto y CTA</div>
  <div class="right">Imagen / multimedia</div>
</div>
<style>
.split {
  display: grid;
  grid-template-columns: 1fr 1fr;
  height: 100vh;
}
.left, .right {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}
@media (max-width: 600px) {
  .split {
    grid-template-columns: 1fr;
  }
}
</style>
```

---

## 5. **Masonry / diseño asimétrico**

```html
<div class="masonry">
  <div class="item tall">Alto</div>
  <div class="item">Normal</div>
  <div class="item wide">Ancho</div>
  <!-- más items -->
</div>
<style>
.masonry {
  display: grid;
  grid-auto-flow: dense;
  grid-template-columns: repeat(auto-fill, minmax(150px,1fr));
  gap: 10px;
}
.item.tall { grid-row: span 2; }
.item.wide { grid-column: span 2; }
</style>
```

---

## 6. **Hero / Full-screen inmersivo**

```html
<section class="hero">
  <div class="overlay">
    <h1>Título impactante</h1>
    <button>Descubre más</button>
  </div>
</section>
<style>
.hero {
  position: relative;
  height: 100vh;
  background: url('tu-imagen.webp') center/cover no-repeat;
}
.overlay {
  position: absolute;
  inset: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
}
</style>
```

---

## 7. **Modular / tarjetas móviles**

```html
<main class="modules">
  <section class="mod">Módulo A</section>
  <section class="mod">Módulo B</section>
  <section class="mod">Módulo C</section>
</main>
<style>
.modules {
  display: grid;
  gap: 1rem;
  grid-template-columns: 1fr;
}
@media (min-width: 640px) {
  .modules {
    grid-template-columns: repeat(2,1fr);
  }
}
@media (min-width: 1024px) {
  .modules {
    grid-template-columns: repeat(3,1fr);
  }
}
.mod {
  padding: 1rem;
  background: #f9f9f9;
  border: 1px solid #ddd;
}
</style>
```

---

### ✅ Buenas prácticas comunes

* **Unidades fluidas**: usa rem, fr, %.
* **Imágenes responsivas**: aplica `max-width:100%`, atributos `srcset`, WebP.
* **Touch-friendly**: botones ≥ 44×44 px.
* **Lazy‑load**: carga diferida de recursos pesados.
* **Mobile‑first**: diseña desde pequeño a grande.

