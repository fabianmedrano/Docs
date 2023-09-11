


2. **DOM (Document Object Model)**:

   ```html
   <!DOCTYPE html>
   <html>
   <head>
     <title>DOM Ejemplo</title>
   </head>
   <body>
     <h1 id="titulo">¡Hola Mundo!</h1>
     <button id="boton">Haz clic</button>

     <script>
       // Selección de elementos del DOM y manipulación
       const tituloElemento = document.getElementById('titulo');
       tituloElemento.textContent = '¡Bienvenidos!';

       const botonElemento = document.getElementById('boton');
       botonElemento.addEventListener('click', () => {
         alert('¡Has hecho clic en el botón!');
       });
     </script>
   </body>
   </html>
   ```