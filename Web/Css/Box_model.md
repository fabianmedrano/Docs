### 2. Box model

El box model es un concepto fundamental en CSS que define cómo se representan visualmente los elementos en la página. Cada elemento se considera una caja que consta de cuatro partes:

- **Contenido**: Es el área donde se muestra el contenido del elemento (texto, imágenes, etc.).

- **Padding**: Es el espacio entre el contenido y el borde. Puedes controlar el padding con las propiedades `padding-top`, `padding-right`, `padding-bottom` y `padding-left`.

- **Borde**: Es la línea que rodea el contenido y el padding. Puedes definir el borde con la propiedad `border`, y ajustar su estilo, grosor y color.

- **Margen**: Es el espacio entre el borde del elemento y otros elementos cercanos. El margen se define con las propiedades `margin-top`, `margin-right`, `margin-bottom` y `margin-left`.

Aquí tienes un ejemplo que ilustra cómo se aplica el box model:

```css
/* Aplica un ancho de 200px, padding de 20px, borde de 2px y margen de 10px */
.mi-elemento {
  width: 200px;
  padding: 20px;
  border: 2px solid black;
  margin: 10px;
}
```
