5. **Trabajar con APIs**:

   ```javascript
   // Uso de una API de ejemplo con XMLHttpRequest (también se puede usar fetch)
   const apiKey = 'tu_clave_de_api';
   const url = `https://api.example.com/data?api_key=${apiKey}`;

   const xhr = new XMLHttpRequest();
   xhr.open('GET', url, true);
   xhr.onload = function () {
     if (xhr.status >= 200 && xhr.status < 300) {
       const data = JSON.parse(xhr.responseText);
       console.log(data);
     } else {
       console.error('Error:', xhr.statusText);
     }
   };
   xhr.onerror = function () {
     console.error('Error de red');
   };
   xhr.send();
   ```
