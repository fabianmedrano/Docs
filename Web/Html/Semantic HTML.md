
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

## Elemento `<main>`

El elemento `<main>` se usa para representar el contenido principal de un documento, que es único y relevante para el propósito de la página. Dentro de él se pueden poner otros elementos semánticos como `<section>`, `<article>`, `<nav>`, etc. Solo puede haber un elemento `<main>` por documento, y no debe estar dentro de `<article>`, `<aside>`, `<footer>`, `<header>` o `<nav>`.

Ejemplo de uso de `<main>`:

```html
<main>
  <section>
    <h2>Contenido principal</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod ...</p>
  </section>
  <section>
    <h2>Otro contenido principal</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod ...</p>
  </section>
</main>
```

## Elemento `<figure>`

El elemento `<figure>` se usa para representar un contenido autocontenido que ilustra, explica o complementa el texto principal, como una imagen, un diagrama, un gráfico, un código, etc. Dentro de él se puede poner un elemento `<figcaption>` para dar un título o una descripción al contenido.

Ejemplo de uso de `<figure>`:

```html
<figure>
  <img src="imagen.jpg" alt="Una imagen">
  <figcaption>Esta es una imagen de ejemplo</figcaption>
</figure>
```

## Elemento `<details>`

El elemento `<details>` se usa para representar un contenido adicional que el usuario puede mostrar u ocultar según su preferencia, como una explicación, una referencia, un comentario, etc. Dentro de él se debe poner un elemento `<summary>` para dar un título o un resumen al contenido, que se muestra siempre. El resto del contenido solo se muestra cuando el usuario hace clic en el elemento `<summary>`.

Ejemplo de uso de `<details>`:

```html
<details>
  <summary>Ver más información</summary>
  <p>Este es un contenido adicional que se puede mostrar u ocultar.</p>
</details>
```

## Elemento `<time>`

El elemento `<time>` se usa para representar una fecha, una hora o una duración en un formato legible por humanos y máquinas. Se recomienda usar el atributo `datetime` para especificar el valor de la fecha o la hora en un formato estándar, como `YYYY-MM-DD` o `HH:MM:SS`.

Ejemplo de uso de `<time>`:

```html
<p>La fecha de hoy es <time datetime="2024-02-13">13 de febrero de 2024</time>.</p>
<p>La hora actual es <time datetime="09:23:01">9:23:01</time>.</p>
<p>La duración del evento es de <time datetime="PT2H30M">2 horas y 30 minutos</time>.</p>
```
.
