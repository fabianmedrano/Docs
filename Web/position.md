# position

1. **Static (Estática)**: Es el valor por defecto de todos los elementos. No se ve afectado por las propiedades `top`, `bottom`, `left` y `right`.

2. **Relative (Relativa)**: El elemento se posiciona en relación a su posición original. Las propiedades `top` y `bottom` especifican el desplazamiento vertical desde su posición original; las propiedades `left` y `right` especifican su desplazamiento horizontal.

3. **Absolute (Absoluta)**: El elemento se posiciona en relación a su bloque contenedor más cercano (que no sea `static`). Las propiedades `top`, `right`, `bottom`, y `left` especifican el desplazamiento desde los bordes del bloque contenedor del elemento.

4. **Fixed (Fija)**: El elemento se posiciona en relación a la ventana del navegador, lo que significa que permanece en el mismo lugar incluso si la página se desplaza.

5. **Sticky (Pegajosa)**: El elemento se comporta como `relative` hasta que su bloque contenedor cruza un límite establecido (como por ejemplo dando a `top` cualquier valor distinto de `auto`), desde el cual es tratado como `fixed`.

