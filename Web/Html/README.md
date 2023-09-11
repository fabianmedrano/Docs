# html

## Flexbox:
Flexbox es un modelo de diseño en CSS que permite organizar elementos dentro de un contenedor de forma flexible, alineándolos y distribuyéndolos en el espacio disponible. Es especialmente útil para diseñar diseños de una dimensión, como alinear elementos en una fila o columna.

Para utilizar Flexbox, primero debes establecer el contenedor como un contenedor flexible mediante la propiedad `display: flex;`. Luego, puedes aplicar diferentes propiedades a los elementos hijos para controlar cómo se distribuyen y alinean dentro del contenedor.

### Propiedades importantes de Flexbox:
`display: flex;` : Esta propiedad se aplica al contenedor y lo convierte en un contenedor flexible. Todos los elementos hijos directos del contenedor se comportarán como elementos flexibles.

#### ` flex-direction `: 
Esta propiedad establece la dirección principal del flujo de los elementos flexibles dentro del contenedor. Puedes usar `row` para una fila (de izquierda a derecha), `column` para una columna (de arriba hacia abajo), `row-reverse `para una fila inversa y `column-reverse` para una columna inversa.

#### ` justify-content:`
 Esta propiedad alinea los elementos flexibles a lo largo del eje principal (según la dirección establecida por `flex-direction`). Puedes usar `flex-start` para alinearlos al inicio, flex-end para alinearlos al final, center para centrarlos, space-between para distribuirlos de manera equitativa con espacios entre ellos, `space-around` para distribuirlos con espacios iguales alrededor de cada elemento y `space-evenly` para distribuirlos con espacios iguales alrededor y entre ellos.

#### `align-items:`
 Esta propiedad alinea los elementos flexibles a lo largo del eje transversal (perpendicular al eje principal). Puedes usar `flex-start` para alinearlos en la parte superior, `flex-end` para alinearlos en la parte inferior, center para centrarlos, baseline para alinearlos según la línea base de su contenido y stretch para estirarlos para que tengan la misma altura que el contenedor.

## CSS Grid:
CSS Grid es otro modelo de diseño en CSS que permite organizar elementos en una cuadrícula bidimensional. Con CSS Grid, puedes definir filas y columnas y colocar elementos dentro de ellas, lo que brinda un mayor control sobre la estructura del diseño.

Para utilizar CSS Grid, primero debes establecer el contenedor como un contenedor de cuadrícula mediante la propiedad `display: grid;`. Luego, puedes definir el diseño de la cuadrícula utilizando las propiedades `grid-template-columns` y `grid-template-rows`.

### Propiedades importantes de CSS Grid:
#### `display: grid;`:
 Esta propiedad se aplica al contenedor y lo convierte en un contenedor de cuadrícula.

#### `grid-template-columns`:
 Esta propiedad define el tamaño de las columnas de la cuadrícula. Puedes especificar los anchos utilizando valores absolutos (por ejemplo, 100px) o fracciones (por ejemplo, 1fr) para distribuir el espacio disponible entre las columnas.

#### `grid-template-rows`: 
Esta propiedad define el tamaño de las filas de la cuadrícula. Al igual que grid-template-columns, puedes usar valores absolutos o fracciones.

#### `grid-gap`:
 Esta propiedad establece el espacio entre las celdas de la cuadrícula. Puedes utilizar px, %, em, etc., para definir el espaciado.

#### `grid-column` y `grid-row`:

 Estas propiedades permiten colocar elementos en celdas específicas de la cuadrícula. Puedes especificar las líneas de inicio y final de la celda donde deseas colocar el elemento.

Estas son solo algunas de las propiedades principales de CSS Grid. Al igual que con Flexbox, hay muchas otras propiedades y funciones más avanzadas que te permiten crear diseños complejos y sofisticados. Puedes consultar la documentación oficial de CSS Grid para obtener más información: https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout