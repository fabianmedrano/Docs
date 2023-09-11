8. **Manejo de errores y depuración**:

   ```javascript
   function dividir(a, b) {
     if (b === 0) {
       throw new Error('No se puede dividir por cero.');
     }
     return a / b;
   }

   try {
     const resultadoDivision = dividir(10, 0);
     console.log(resultadoDivision);
   } catch (error) {
     console.error('Error:', error.message);
   }
   ```