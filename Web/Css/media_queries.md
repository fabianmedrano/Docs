
### 6. Media queries

---

## ✅ Media Queries Responsivas Esenciales

### 📱 Móviles (hasta 480 px)

```css
@media (max-width: 480px) {
  /* Estilos para móviles muy pequeños (iPhone SE, Galaxy Fold) */
}
```

### 📱 Móviles estándar (481px a 767px)

```css
@media (min-width: 481px) and (max-width: 767px) {
  /* Smartphones normales en vertical */
}
```

### 📲 Tablets en vertical (768px a 1023px)

```css
@media (min-width: 768px) and (max-width: 1023px) {
  /* iPad vertical, tablets medianos */
}
```

### 💻 Tablets en horizontal / Laptops pequeños (1024px a 1279px)

```css
@media (min-width: 1024px) and (max-width: 1279px) {
  /* Tablets en horizontal, laptops chicos */
}
```

### 🖥️ Escritorio estándar (1280px a 1439px)

```css
@media (min-width: 1280px) and (max-width: 1439px) {
  /* Resoluciones estándar de escritorio */
}
```

### 🖥️ Escritorio ancho / pantallas grandes (1440px a 1919px)

```css
@media (min-width: 1440px) and (max-width: 1919px) {
  /* Monitores HD, pantallas grandes */
}
```

### 🖥️ Ultra HD / 4K+ (1920px en adelante)

```css
@media (min-width: 1920px) {
  /* Pantallas 4K o superiores */
}
```

---

## 🧠 Tip: Mobile-first (mejor práctica)

1. Escribe primero los estilos base para pantallas pequeñas.
2. Luego usa `@media (min-width: …)` para escalar hacia pantallas mayores.

```css
/* Base (móviles primero) */
.container {
  padding: 1rem;
}

/* Tablet en adelante */
@media (min-width: 768px) {
  .container {
    padding: 2rem;
  }
}
```

---

## 🧰 ¿Qué unidades usar?

* Usa `rem` o `em` para márgenes, paddings, fuentes.
* Usa `%`, `fr`, o `clamp()` para anchos y contenedores.

---

## 🚀 BONUS: Breakpoints Tailwind (por si te interesa)

| Nombre | Rango px |
| ------ | -------- |
| `sm`   | ≥640px   |
| `md`   | ≥768px   |
| `lg`   | ≥1024px  |
| `xl`   | ≥1280px  |
| `2xl`  | ≥1536px  |

---


