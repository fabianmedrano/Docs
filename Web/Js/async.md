4. **Asincronía**:

   ```javascript
   // Uso de Promises para realizar una petición HTTP
   fetch('https://jsonplaceholder.typicode.com/posts/1')
     .then(response => response.json())
     .then(data => console.log(data))
     .catch(error => console.error('Error:', error));

   // Uso de async/await para hacer la misma petición
   async function obtenerDatos() {
     try {
       const response = await fetch('https://jsonplaceholder.typicode.com/posts/1');
       const data = await response.json();
       console.log(data);
     } catch (error) {
       console.error('Error:', error);
     }
   }

   obtenerDatos();
   ```
