
### 4. Flexbox

Flexbox es una poderosa herramienta para crear diseños flexibles y responsivos. Es especialmente útil para alinear y distribuir elementos en un contenedor. Algunas propiedades de Flexbox son:

- **`display: flex`**: Establece el contenedor como un contenedor flexible, permitiendo que los elementos internos se comporten como flex items.

- **`flex-direction`**: Define la dirección principal en la que los elementos se distribuyen. Los valores pueden ser `row` (de izquierda a derecha), `column` (de arriba hacia abajo), `row-reverse` o `column-reverse`. Por defecto es row

- **`justify-content`**: Controla el alineamiento de los elementos flexibles en la dirección principal. Por ejemplo, `justify-content: center` centrará los elementos.

- **`align-items`**: Controla la alineación de los elementos flexibles en la dirección secundaria. Por ejemplo, `align-items: center` centrará verticalmente los elementos.
 
- **`flex-wrap: wrap`**: Permite que los elementos, se desborden en filas inferiores y sobre solo una fila

- **`flex-flow`**: Combina `flex-wrap` y  `flex-direction`
```html
<nav class="menu">
  <a href="#">Inicio</a>
  <a href="#">Acerca de</a>
  <a href="#">Contacto</a>
</nav>
```

```css
/* Estilos para el menú utilizando Flexbox */
.menu {
  display: flex;
  justify-content: space-around;
  background-color: #333;
  color: #fff;
  padding: 10px;
}

.menu a {
  text-decoration: none;
  color: #fff;
}
```
