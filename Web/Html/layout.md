
1. **Diseño Fluid Grid**: Este método se basa en el uso de porcentajes para especificar anchos en lugar de píxeles fijos. Aquí tienes un ejemplo básico¹:

```html
<div class="container">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>
```
```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
}

.box {
  border: 1px solid black;
  padding: 1em;
}
```

2. **Media Queries**: Las media queries permiten aplicar diferentes estilos CSS dependiendo de las características del dispositivo. Aquí tienes un ejemplo básico⁴:

```css
body {
  background-color: blue;
}

@media screen and (min-width: 600px) {
  body {
    background-color: olive;
  }
}

@media screen and (min-width: 992px) {
  body {
    background-color: tan;
  }
}
```

3. **Imágenes Flexibles**: Las imágenes flexibles se redimensionan dentro de su contenedor para evitar que se desborden cuando la ventana del navegador se reduce. Aquí tienes un ejemplo básico⁹:

```css
img {
  max-width: 100%;
  height: auto;
}
```

4. **Marcos de trabajo responsivos**: Existen marcos de trabajo CSS, como Bootstrap, que proporcionan una estructura básica que es responsiva por defecto. Aquí tienes un ejemplo básico usando Bootstrap:

```html
<div class="container">
  <div class="row">
    <div class="col-sm">
      Columna 1
    </div>
    <div class="col-sm">
      Columna 2
    </div>
    <div class="col-sm">
      Columna 3
    </div>
  </div>
</div>
```

5. **CSS Flexbox**: Flexbox es una técnica de CSS que permite crear diseños flexibles y responsivos. Aquí tienes un ejemplo básico¹⁶:

```html
<div class="container">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>
```
```css
.container {
  display: flex;
  justify-content: space-between;
}

.box {
  flex: 1 1 auto;
  margin: 1em;
  padding: 1em;
  border: 1px solid black;
}
```

6. **CSS Grid**: CSS Grid es una técnica de CSS que permite crear diseños de cuadrícula complejos que son responsivos. Aquí tienes un ejemplo básico²⁴:

```html
<div class="grid-container">
  <div class="grid-item">1</div>
  <div class="grid-item">2</div>
  <div class="grid-item">3</div>
  <div class="grid-item">4</div>
  <div class="grid-item">5</div>
  <div class="grid-item">6</div>
</div>
```
```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  grid-gap: 1em;
}

.grid-item {
  border: 1px solid black;
  padding: 1em;
}
```

