
### 9. Transiciones y animaciones

Las transiciones y animaciones permiten agregar interactividad y dinamismo a una página web. Aquí algunos detalles importantes:

- **Transiciones**: Permiten suavizar cambios de estilo en un elemento cuando ocurren ciertos eventos, como al pasar el cursor sobre un elemento (`:hover`). Se definen con la propiedad `transition` y sus subpropiedades (`transition-property`, `transition-duration`, `transition-timing-function` y `transition-delay`).

- **Animaciones**: Son secuencias de transiciones que crean efectos más complejos y continuos. Se definen con la propiedad `@keyframes` para establecer los estados clave de la animación y luego se aplican con `animation`.

Ejemplo:

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

En este ejemplo, al pasar el cursor sobre `.mi-elemento`, la opacidad del elemento cambia gradualmente durante 0.5 segundos, creando un efecto de desvanecimiento.


