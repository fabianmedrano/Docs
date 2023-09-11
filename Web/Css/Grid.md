
### 5. Grid

CSS Grid es otra herramienta para crear diseños más complejos y estructurados en dos dimensiones. Con CSS Grid, puedes dividir la página en filas y columnas, y colocar elementos en celdas específicas. Algunas propiedades de CSS Grid son:

- **`display: grid`**: Establece el contenedor como un contenedor de rejilla, permitiendo que los elementos internos se comporten como elementos de la rejilla.

- **`grid-template-columns`**: Define el ancho de las columnas en la rejilla.

- **`grid-template-rows`**: Define la altura de las filas en la rejilla.

- **`grid-gap`**: Especifica el espacio entre las celdas de la rejilla.

Aquí tienes un ejemplo de cómo usar CSS Grid para crear un diseño de dos columnas:



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

En este ejemplo, el contenedor se establece como una rejilla con tres columnas de igual tamaño (`1fr` significa que cada columna ocupará el mismo espacio disponible) y un espacio de 10px entre cada elemento. Los elementos dentro del contenedor se distribuirán automáticamente en las columnas de la rejilla.

### Posicionamiento de elementos

Con CSS Grid, puedes determinar la posición de un elemento utilizando las propiedades `grid-column` y `grid-row`. Estas propiedades te permiten especificar en qué columna y fila debe ubicarse el elemento dentro de la cuadrícula.

Por ejemplo, si quieres colocar un elemento en la segunda columna y la primera fila de una cuadrícula, puedes hacerlo de la siguiente manera:

```css
.item {
  grid-column: 2;
  grid-row: 1;
}
```

También puedes utilizar las propiedades `grid-column-start`, `grid-column-end`, `grid-row-start` y `grid-row-end` para especificar en qué celda debe comenzar y terminar el elemento. Por ejemplo, si quieres que un elemento ocupe dos columnas y una fila, puedes hacerlo de la siguiente manera:

```css
.item {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 2;
}
```

