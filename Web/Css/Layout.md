
### 3. Layout

El diseño o layout en CSS es la forma en que los elementos se colocan en la página. Hay varios métodos para controlar el diseño, como el posicionamiento y la propiedad `display`. Algunos ejemplos son:

- **Posicionamiento relativo y absoluto**: El posicionamiento permite controlar la ubicación de un elemento en relación con su posición original. Los elementos con posicionamiento relativo se desplazan respecto a su posición normal, mientras que los elementos con posicionamiento absoluto se posicionan respecto a su elemento padre con posicionamiento relativo o al contenedor principal (`<body>`). Aquí tienes un ejemplo:

```html
<div class="contenedor">
  <div class="elemento1">Elemento 1</div>
  <div class="elemento2">Elemento 2</div>
</div>
```

```css
/* Posicionamiento absoluto */
.elemento1 {
  position: absolute;
  top: 50px;
  left: 50px;
}

/* Posicionamiento relativo */
.elemento2 {
  position: relative;
  top: 20px;
  left: 20px;
}
```

- **Propiedad `display`**: La propiedad `display` define cómo se muestran los elementos en la página. Los valores más comunes son `block`, `inline`, `inline-block`, `flex`, `grid`, entre otros. Por ejemplo, utilizando `display: flex` podemos crear diseños flexibles y responsivos:

```html
<div class="contenedor">
  <div class="elemento">Elemento 1</div>
  <div class="elemento">Elemento 2</div>
  <div class="elemento">Elemento 3</div>
</div>
```

```css
/* Contenedor con flexbox */
.contenedor {
  display: flex;
  justify-content: space-between;
}

/* Estilos de los elementos */
.elemento {
  flex: 1;
  padding: 10px;
  background-color: lightblue;
}
```
