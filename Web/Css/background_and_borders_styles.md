
### 8. Estilos de fondo y bordes

Los estilos de fondo y bordes pueden mejorar significativamente la apariencia visual de los elementos. Aquí tienes algunos detalles:

- **`background-color`**: Define el color de fondo de un elemento.

- **`background-image`**: Permite agregar una imagen como fondo. Puedes usar la propiedad `url()` para especificar la ruta de la imagen.

- **`border`**: Controla el borde del elemento y combina las propiedades de `border-width`, `border-style` y `border-color`.

- **`border-radius`**: Permite crear bordes redondeados. Puedes especificar un valor en píxeles o porcentajes.

Ejemplo:

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
