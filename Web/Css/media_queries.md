
### 6. Media queries

Las media queries permiten aplicar estilos específicos según el tamaño de la pantalla o el dispositivo en el que se visualiza la página. Esto es fundamental para crear diseños responsivos que se adapten a diferentes tamaños de pantalla.

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

En este ejemplo, se establece que el texto de los elementos tenga un tamaño de 20px en pantallas grandes, pero si el ancho de la pantalla es igual o menor a 768px, se aplicará un tamaño de texto de 16px.
