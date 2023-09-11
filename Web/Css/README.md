



## CSS para desarrolladores junior

### 1. Selectores

Los selectores son patrones que se utilizan para seleccionar elementos HTML y aplicarles estilos. Aquí tienes algunos ejemplos:

- **Selector de tipo**: Aplica estilos a todos los elementos de un tipo específico, por ejemplo, todos los párrafos `<p>`:

```css
p {
  color: blue;
}
```

- **Selector de clase**: Aplica estilos a elementos con una clase específica, por ejemplo, elementos con la clase "destacado":

```css
.destacado {
  font-weight: bold;
}
```

- **Selector de ID**: Aplica estilos a un único elemento con un ID específico, por ejemplo, un elemento con el ID "encabezado":

```css
#encabezado {
  background-color: gray;
}
```

### 2. Box model

El box model se refiere al modelo de caja que tienen todos los elementos en CSS, y consta de contenido, padding, borde y margen. Aquí hay un ejemplo:

```css
/* Aplica un ancho de 200px, padding de 20px, borde de 2px y margen de 10px */
.mi-elemento {
  width: 200px;
  padding: 20px;
  border: 2px solid black;
  margin: 10px;
}
```

### 3. Layout

El posicionamiento y la propiedad `display` son fundamentales para el diseño en CSS. Aquí tienes un ejemplo con posicionamiento:

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

### 4. Flexbox

[más información](Flexbox/Flexbox.md)

Flexbox es una forma poderosa de crear diseños flexibles. Aquí hay un ejemplo simple:

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

### 5. Grid

El sistema de rejilla de CSS permite un diseño más estructurado. Aquí hay un ejemplo:

```html
<div class="contenedor">
  <div class="elemento">Elemento 1</div>
  <div class="elemento">Elemento 2</div>
  <div class="elemento">Elemento 3</div>
</div>
```

```css
/* Contenedor con grid */
.contenedor {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 10px;
}

/* Estilos de los elementos */
.elemento {
  padding: 10px;
  background-color: lightblue;
}
```

### 6. Media queries

Las media queries permiten aplicar estilos diferentes según el tamaño de la pantalla. Aquí hay un ejemplo:

```css
/* Estilos para pantallas grandes */
.elemento {
  font-size: 20px;
}

/* Estilos para pantallas pequeñas */
@media (max-width: 768px) {
  .elemento {
    font-size: 16px;
  }
}
```

Esto cambiará el tamaño del texto a 20px para pantallas grandes y a 16px para pantallas pequeñas (menores o iguales a 768px de ancho).

Recuerda que la práctica constante y la experimentación con ejemplos reales te ayudarán a mejorar tus habilidades en CSS y a enfrentar desafíos cada vez más complejos en el desarrollo web. ¡Buena suerte en tu aprendizaje!
¡Claro! Continuemos con los demás puntos:

### 7. Tipografía

Aprender a manipular la tipografía en CSS es importante para mejorar la legibilidad y el aspecto general de un sitio web. Aquí tienes un ejemplo:

```css
/* Cambiar el tipo de fuente y tamaño */
body {
  font-family: "Arial", sans-serif;
  font-size: 16px;
}

/* Cambiar el color del texto */
h1 {
  color: #333;
}

/* Aplicar negrita al texto */
strong {
  font-weight: bold;
}
```

### 8. Estilos de fondo y bordes

Los estilos de fondo y bordes pueden mejorar la apariencia visual de los elementos en una página. Aquí tienes un ejemplo:

```css
/* Establecer un fondo con color */
.mi-elemento {
  background-color: #f2f2f2;
}

/* Agregar una imagen de fondo */
.encabezado {
  background-image: url("imagen.jpg");
  background-size: cover;
}

/* Aplicar bordes redondeados */
.imagen-avatar {
  border-radius: 50%;
  width: 100px;
  height: 100px;
}
```

### 9. Transiciones y animaciones

Las transiciones y animaciones permiten agregar interactividad y dinamismo a una página web. Aquí hay un ejemplo de una animación de desvanecimiento:

```css
/* Establecer el estado inicial */
.mi-elemento {
  opacity: 1;
  transition: opacity 0.5s;
}

/* Establecer el estado final con la animación */
.mi-elemento:hover {
  opacity: 0.5;
}
```

### 10. Compatibilidad entre navegadores

Es esencial tener en cuenta las diferencias de compatibilidad entre navegadores y aplicar soluciones adecuadas. Es común usar herramientas como "caniuse.com" para verificar la compatibilidad de las propiedades CSS.

### 11. Prácticas de organización

Mantener el código CSS bien organizado facilita su mantenimiento y escalabilidad. Aquí tienes un ejemplo de cómo usar la metodología BEM para nombrar clases:

```html
<div class="card">
  <h2 class="card__title">Título</h2>
  <p class="card__content">Contenido</p>
</div>
```

```css
/* Estilos utilizando la metodología BEM */
.card {
  /* Estilos del contenedor de la tarjeta */
}

.card__title {
  /* Estilos del título de la tarjeta */
}

.card__content {
  /* Estilos del contenido de la tarjeta */
}
```

### 12. Uso de herramientas

El uso de preprocesadores CSS como Sass o Less puede facilitar el proceso de desarrollo. Aquí tienes un ejemplo de Sass:

```scss
/* Definición de variables */
$color-primario: #007bff;

/* Uso de variables */
.boton {
  background-color: $color-primario;
  color: #fff;
}
```

### 13. Accesibilidad

Considerar la accesibilidad en el diseño de la interfaz es crucial para garantizar que todos los usuarios puedan interactuar con el sitio. Asegúrate de utilizar etiquetas semánticas, colores con contraste adecuado y proporcionar alternativas para elementos multimedia.

### 14. Buenas prácticas

Adoptar buenas prácticas de desarrollo, como el uso de un reset CSS para igualar el comportamiento de los navegadores, evitar el uso excesivo de estilos en línea y mantener una hoja de estilos limpia y concisa.

Recuerda que la práctica, la experimentación y la exploración son fundamentales para mejorar tus habilidades como desarrollador junior de CSS. ¡Buena suerte en tu aprendizaje y desarrollo!
