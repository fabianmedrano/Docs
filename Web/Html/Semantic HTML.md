
#  HTML semántico

## Elemento `<header>`

El elemento `<header>` se usa para representar el encabezado de un documento o una sección. Dentro de él se pueden poner elementos de título (`<h1>` a `<h6>`), imágenes, párrafos o listas de navegación.

Ejemplo de uso de `<header>`:

```html
<header>
  <h1>Título de la página</h1>
  <h2>Subtítulo de la página</h2>
</header>
```

## Elemento `<section>`

El elemento `<section>` se usa para representar una sección temática dentro de un documento. Cada sección suele tener un título, que se define con un elemento de título.

Ejemplo de uso de `<section>`:

```html
<section>
  <h3>Sección 1</h3>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod ...</p>
</section>
```

## Elemento `<article>`

El elemento `<article>` se usa para representar un contenido independiente y autocontenido, que tiene sentido por sí mismo y se puede distribuir aparte del resto de la web. Un ejemplo típico son los artículos de un blog o las noticias de un periódico. Se recomienda identificar cada `<article>` con un título.

Ejemplo de uso de `<article>`:

```html
<article>
  <h3>Título del artículo 1</h3>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod ...</p>
</article>
<article>
  <h3>Título del artículo 2</h3>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod ...</p>
</article>
```

## Elemento `<nav>`

El elemento `<nav>` se usa para representar un conjunto de enlaces de navegación, que se crean con los elementos `<ul>`, `<li>` y `<a>`. Se puede usar en cualquier parte de la web que contenga una lista de enlaces, como el encabezado, el pie de página o el menú lateral.

Ejemplo de uso de `<nav>`:

```html
<nav>
  <ul>
    <li><a href="#">Página 1</a></li>
    <li><a href="#">Página 2</a></li>
    <li><a href="#">Página 3</a></li>
    <li><a href="#">Página 4</a></li>
  </ul>
</nav>
```

## Elemento `<aside>`

El elemento `<aside>` se usa para representar un contenido secundario o adicional al contenido principal. Por ejemplo, una caja de información, una publicidad, una cita o una nota al margen.

Ejemplo de uso de `<aside>`:

```html
<aside>
  <p>Este es un contenido adicional que no forma parte del contenido principal.</p>
</aside>
```

## Elemento `<footer>`

El elemento `<footer>` se usa para representar el pie de página de un documento o una sección. Dentro de él se pueden poner elementos de información, como el autor, la fecha, los derechos de autor, los enlaces de contacto o las redes sociales.

Ejemplo de uso de `<footer>`:

```html
<footer>
  <p>© 2024 Todos los derechos reservados.</p>
  <p>Contacto: ejemplo@correo.com</p>
</footer>
```
